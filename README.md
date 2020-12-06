
# Verifying Integrity

- Let's Check Our Data
1. Possible merging issue:

a. Unintentional 'one-to-many' relationship
b. Unintentional 'many-to-many' relationship

2. Possible concatenating issue:

a. Duplicate records possibly unintentionally introduced

- Validating Merges
.merge(validate=None)
1. Check if merge is of specified type:
one_to_one
one_to_many
many_to_one
many_to_many

- Merge Validate : One-to-One

tracks.merge(specs, on='tid', validate='one_to_one')

---> Returns Errors, which means the validation type is not one to one type

tracks.merge(specs, on='tid', validate='one_to_many')

---> Returns values

- Verifying Concatenations
.concat(verify_integrity=False)
a. Check whether the new concatenated index contains duplicates
b. Default value is False

- Verifying Concatenation: Example
pd.concate([inv_feb, inv_mar], verify_integrity=True)

---> Returns Errors, which means there are duplicates within the concatenations

pd.concate([inv_feb, inv_mar], verify_integrity=False)

- Why Verify Integrity and What to Do
Why:
Real world data is not often clean

What to do:
a. Fix incorrect data
b. Drop duplicate rows





