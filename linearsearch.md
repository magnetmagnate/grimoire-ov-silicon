# An Incantation to Discover the Position ov an Element ov a List Which, the List Being Already in One's Possession, Coincides in Value With an Input to be Provided, or, If There Be No Such Value, Indicate the Lack Thereof.

Suppose thou possess an unsorted list ov some few elements and wish to discover whether an element ov known value exists within the aforementioned list, and if so, at what location. Herein lies the answer to thy conundrum: incant a spell which, starting from one end ov the list to be searched, observes each element in turn, checking for equivalence to the desired value, one at a time, completing when the desired element is located or when all elements have been observed and found unequal to the value sought. In the latter case, the spell must indicate the failure of the search in some fashion, such as by returning a `null` value or an index outside the range ov the list.

Here follows an example ov such a spell in the venerable High Speech ov `C`. It must be noted that, should the `array` hold more than a single `int` matching the desired value, it is the index ov the earliest such instance that shall be found.
```C
int FindFirst(int *array, int array_len, int target)
{
    for (int i = 0; i < array_len; ++i)
    {
        if (*(array + i) == target)
        {
            /* that which was desired is now in our grasp */
            return i;
        }
    }
    /* that which was sought existeth not */
    return -1;
} /* thus ends the incantation */
```

Behold now a similar spell, whose result differs from the above in the case that there be more than a single correct result. In the version that follows, it is the latest, rather than the earliest, index to satisfy the condition that shall be found. Attend well to the subtle differences, lest thy result be incorrect.

```C
int FindLast (int *array, int array_len, int target)
{
    for (int i = array_len; i > 0; )
    {
        --i;
        if (array[i] == target)
        {
            return i;
        }
    }
    return -1;
}
```
<!--TODO: add versions in different, higher level & functional languages -->

>further explanation of performance characteristics, etc.

>praise to the Omnissiah
