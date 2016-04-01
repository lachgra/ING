# ING
It's no Google

    Copyright (C) 2016 Lachlan Grant
    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.

    You can contact me via email:
    lachie.g.j@gmail.com


This program, given a text file of arbitrary size,
searches for the line which resembles the search term
as closely as possible. ING will return a rank
of the lines in the text which achieved the highest level 
of similarity.

Resemblance is defined by the number of consecutively
correct characters a line has with respect to a query.

However, the part of the line which matches the query
could be a subset of the query, in fact it happens to be
that even for large texts, queries of more than a few words
often will not be matched. This is the advantage that ING
has over a binary "yes this is a match" or "no it is not" 
algorithm.

In short, ING will check all possible consecutive subsets of 
the lineagainst all possible subsets of our query. 

My goal with ING is to implement more complexity to get_score(), 
allowing us to check a variable number of parts of the line 
for subsets of our query.

For example:
Source = "ING's no Google"
Query  = "ING"

Output:

--------------------------------------------------

Length of your Query is 3...
Thus 3 is the highest possible score

--------------------------------------------------
1: Line    1, score = 3
ING's no Google
---
2: Line    2, score = 0

---

--------------------------------------------------

To do: More complexity.

