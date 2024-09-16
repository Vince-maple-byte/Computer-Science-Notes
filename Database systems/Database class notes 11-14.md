#### Informal Design Guidelines for relational schema
- Making sure that the semantics of the attributes are clear in the schema
- Reducing the redundant information in tuples
- Reducing the NULL values in tuples
- Disallowing the possibility of generating spurious tuples
# Functional Dependency
A functional dependency, denoted by X -> Y, between two sets of attributes X and Y that are subsets of R specifies a constraint on the possible tuples that can form a relation state r of R.

# Normalization of Data
The normalization process, takes a relation schema through a series of test to certify whether it satisfies a certain normal form. (Need to study normalization)

# Superkey
A superkey of a relation schema R = {A1, A2,..., AN} is a set of attributes S $\subseteq$ R with the property that no two tuples t1 and t2 in any legal relation state r of the R will t1[S] = t2[S].
	- A super key uniquely identifies a row.
	- A super key could contain additional attributes that are not necessary for unique identification.

$$

$$
#databases 