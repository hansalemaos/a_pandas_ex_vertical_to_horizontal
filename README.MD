# Vertical to horizontal (Series to DataFrame with multiple columns)

```python
pip install a-pandas-ex-vertical-to-horizontal
from a_pandas_ex_vertical_to_horizontal import pd_add_vertical_to_horizontal
pd_add_vertical_to_horizontal()

df = pd.concat(
    [pd.Series(range(0, 20)), pd.Series(range(1000, 1020))], axis=0
).reset_index(drop=True)


df1 = df.s_vertical_to_horizontal(number_of_cells_to_join=3, drop_redundant=False, negative=False)
df2 = df.s_vertical_to_horizontal(number_of_cells_to_join=6, drop_redundant=True, negative=True)




print(df.to_string())
0        0
1        1
2        2
3        3
4        4
5        5
6        6
7        7
8        8
9        9
10      10
11      11
12      12
13      13
14      14
15      15
16      16
17      17
18      18
19      19
20    1000
21    1001
22    1002
23    1003
24    1004
25    1005
26    1006
27    1007
28    1008
29    1009
30    1010
31    1011
32    1012
33    1013
34    1014
35    1015
36    1016
37    1017
38    1018
39    1019


print(df1.to_string())
    col_0  col_1  col_2
0       0   1019   1018
1       1      0   1019
2       2      1      0
3       3      2      1
4       4      3      2
5       5      4      3
6       6      5      4
7       7      6      5
8       8      7      6
9       9      8      7
10     10      9      8
11     11     10      9
12     12     11     10
13     13     12     11
14     14     13     12
15     15     14     13
16     16     15     14
17     17     16     15
18     18     17     16
19     19     18     17
20   1000     19     18
21   1001   1000     19
22   1002   1001   1000
23   1003   1002   1001
24   1004   1003   1002
25   1005   1004   1003
26   1006   1005   1004
27   1007   1006   1005
28   1008   1007   1006
29   1009   1008   1007
30   1010   1009   1008
31   1011   1010   1009
32   1012   1011   1010
33   1013   1012   1011
34   1014   1013   1012
35   1015   1014   1013
36   1016   1015   1014
37   1017   1016   1015
38   1018   1017   1016
39   1019   1018   1017


print(df2.to_string())
    col_0  col_1  col_2  col_3  col_4  col_5
0       0      1      2      3      4      5
6       6      7      8      9     10     11
12     12     13     14     15     16     17
18     18     19   1000   1001   1002   1003
24   1004   1005   1006   1007   1008   1009
30   1010   1011   1012   1013   1014   1015
36   1016   1017   1018   1019      0      1
```