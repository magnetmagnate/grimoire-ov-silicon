# An Incantation to Discover the Position ov an Element ov a List Which, the List Being Already in One's Possession, Coincides in Value With an Input to be Provided, or, If There Be No Such Value, Indicate the Lack Thereof.

>information about the purpose of the incantation and appropriate times for use goes here

```C
int LinearSearch(int *array, int array_len, int target)
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

>further explanation of performance characteristics, etc.

>praise to the Omnissiah
