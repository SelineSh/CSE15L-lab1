Part 1

A failure-inducing input for the buggy program, 
as a JUnit test and any associated code:

```
  @Test
  public void testReversed() {
    int[] input1 = { 4, 8, 5, 6};
    assertArrayEquals(new int[]{6, 5, 8, 4}, ArrayExamples.reversed(input1));
  }
```


An input that doesn’t induce a failure,
as a JUnit test and any associated code 

```
 @Test
  public void testReversed() {
    int[] input1 = { };
    assertArrayEquals(new int[]{ }, ArrayExamples.reversed(input1));
  }
```

The symptom, as the output of running the tests 
![Image](3-1.jpg)

The bug, as the before-and-after code change required to fix it

Before:

``` 
static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      arr[i] = newArray[arr.length - i - 1];
    }
    return arr;
  }
```

After:

```
    static int[] reversed(int[] arr) {
    int[] newArray = new int[arr.length];
    for(int i = 0; i < arr.length; i += 1) {
      newArray[i] = arr[arr.length - i - 1];
    }
    return newArray;
  }
```

Before the change, the code tries to make ```arr``` 
equal to the flipped ```newArray```. But the ```newArray``` 
doesn't have any content inside it, it only has 
the same length as ```arr```. Only ```arr``` has content 
inside. So it should be ```newArray``` as the save place 
to store the flipped ```arr```.


Part 2

``` grep -c``` 

The ```grep``` command is used to search for patterns in text.

The ```-c``` option is used to count the number of lines that match the pattern.

```
$ grep -c "All" ./technical/biomed/1468-6708-3-1.txt
    3
```
This command looks for the match string ```All``` in technical/biomed/1468-6708-3-1.txt and notes how many lines there are, and prints out the number. It is used to know how many lines appear string ``All`` in the file.

```
$ grep -c "way" ./technical/biomed/1468-6708-3-1.txt
    2
```

This command looks for the match string ```way``` in technical/biomed/1468-6708-3-1.txt and notes how many lines there are, and prints out the number. It is used to know how many lines appear string ```way``` in the file.

```grep -w```

The ```grep``` command is used to search for patterns in text.

The ```-w``` option is used to search patterns in the text. And make sure that it is matching a complete word, not a part of it. Then print the line of the matching line

```
$ grep -w "All" ./technical/biomed/1468-6708-3-1.txt
        for relevant covariates [ 1 2 3 4 5 6 ] . All studies found
          All analyses were performed separately for men and
```

This command searches technical/biomed/1468-6708-3-1.txt for how many whole words ```All``` and prints the line where the word ```All``` appears. It's used to only look for the word ```All```, and doesn't want to look for All as part of a word.

```
$ grep -w "way" ./technical/biomed/1468-6708-3-1.txt
          in a consistent way with health suggests that such
```

This command searches technical/biomed/1468-6708-3-1.txt for how many whole words ```way``` and prints the line where the word ```way``` appears. It's used to only look for the word ```way```and doesn't want to look for way as part of a word.

```grep -n```

The ```grep``` command is used to search for patterns in text.

The ```-n``` option is used to search for pattern in the text and print the line number and line of the matching line.

```
$ grep -n "All" ./technical/biomed/1468-6708-3-1.txt
12:        for relevant covariates [ 1 2 3 4 5 6 ] . All studies found
150:          All analyses were performed separately for men and
319:          24-30 for persons aged 60 to 69 [ 8 ] . Allison 
```
This command searches for the string ```All``` in technical/biomed/1468-6708-3-1.txt and prints the contents and line numbers of the matching lines. It is used to make it easier to know on which line the string ```All``` appears.


```
$ grep -n "way" ./technical/biomed/1468-6708-3-1.txt
307:        different ways of coding YHL. The only substantive change
345:          in a consistent way with health suggests that such
```
This command searches for the string ```way``` in technical/biomed/1468-6708-3-1.txt and prints the contents and line numbers of the matching lines. It is used to make it easier to know on which line the string ```way``` appears.


```grep -i```

The ```grep``` command is used to search for patterns in text.

The ```-i ``` option is used to search case-insensitively and print the contents of matching lines.

```
$ grep -i "All" ./technical/biomed/1468-6708-3-1.txt
        for relevant covariates [ 1 2 3 4 5 6 ] . All studies found
        in certain small subsets. A review of 13 studies of older
        throughout adult life. It may be that a small amount of
        number of studies of older persons is fairly small, and
          for all subjects using a baseline home interview, an
          follow-up (n = 5,201) and the second (all African
          Data collection began in 1989, and follow-up is virtually
          complete for all surviving subjects [ 12 ] .
          death, since all are considered 'not healthy'. We also
          10% of the sample). We performed all analyses with and
          without the persons who had partially estimated data, to
          All analyses were performed separately for men and
          second on all of the covariates listed above. We
          have been causally affected by the person's weight. We
          intervals or analysis of variance. Finally we calculated
        men were most likely to have unintentionally lost more than
        statistically significant (p <.05) except for BMI and
        the difference in BMI was no longer statistically
        adjusted for all covariates, is not very different (the
        with 20-24.9 in all comparisons. For this reason, and to
        different. The bars are slightly offset to permit all error
        classified as normal, overweight or obese all had about the
        statistically significant. YHL was significantly higher for
        to normal yielded small, non-significant effect sizes, with
        the persons with partially estimated data, and using two
        shown in Table 1were no longer statistically significant,
        due to a smaller sample size.
          24-30 for persons aged 60 to 69 [ 8 ] . Allison 
          evaluations should be considered critically when older
          higher weight are especially unclear, and the optimal
          outcome measure. Both YOL and YHL would be clinically
          appropriate here, since virtually no persons were lost to
          designed specifically to measure those conditions might
        older adults, especially for women. Future efforts to
```
This command searches for all case-insensitive strings ``All`` in technical/biomed/1468-6708-3-1.txt and prints the contents of the matching lines. Use this command to find out on which lines the case-insensitive string ``All`` appears.



```
grep -i "way" ./technical/biomed/1468-6708-3-1.txt
        different ways of coding YHL. The only substantive change
          in a consistent way with health suggests that such
```

This command searches for all case-insensitive strings ``way`` in technical/biomed/1468-6708-3-1.txt and prints the contents of the matching lines. Use this command to find out on which lines the case-insensitive string ``way`` appears.

