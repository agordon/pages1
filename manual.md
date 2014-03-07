---
layout: default
title: pages1 - Manual
---

### Calc Usage

Run `calc --help` to see the help screen:

```sh
$ calc --help
Usage: ./calc [OPTION] op col [op col ...]
Performs numeric/string operations on input from stdin.

'op' is the operation to perform on field 'col'.

Numeric operations:
  count      count number of elements in the input group
  sum        print the sum the of values
  min        print the minimum value
  max        print the maximum value
  absmin     print the minimum of abs(values)
  absmax     print the maximum of abs(values)
  mean       print the mean of the values
  median     print the median value
  mode       print the mode value (most common value)
  antimode   print the anti-mode value (least common value)
  pstdev     print the population standard deviation
  sstdev     print the sample standard deviation
  pvar       print the population variance
  svar       print the sample variance

String operations:
  unique     print comma-separated sorted list of unique values
  uniquenc   Same as above, while ignoring upper/lower case letters.
  collapse   print comma-separed list of all input values


General options:
  -f, --full                Print entire input line before op results
                            (default: print only the groupped keys)
  -g, --groups=X[,Y,Z,]     Group via fields X,[Y,X]
                            This is a short-cut for --key:
                            '-g5,6' is equivalent to '-k5,5 -k6,6'
  --header-in               First input line is column headers
  --header-out              Print column headers as first line
  -H, --headers             Same as '--header-in --header-out'
  -s, --sort                Sort the input before grouping
                            Removes the need to manually pipe the input through 'sort'
  -t, --field-separator=X   use X instead of whitespace for field delimiter
  -T                        Use tab as field separator
                            Same as -t $'\t'
  -z, --zero-terminated     end lines with 0 byte, not newline
      --help     display this help and exit
      --version  output version information and exit

Examples:

Print the mean and the median of values from column 1:

  $ seq 10 | ./calc mean 1 median 1

Group input based on field 1, and sum values (per group) on field 2:

  $ printf "%s %d\n" A 10 A 5 B 9 | ./calc -g1 sum 2

Unsorted input must be sorted:

  $ cat INPUT.TXT | ./calc -s -g1 mean 2

  Which is equivalent to:
  $ cat INPUT.TXT | sort -k1,1 | ./calc -g1 mean 2
```

More details and examples here

See more examples in the [Examples Section](./examples.html).

