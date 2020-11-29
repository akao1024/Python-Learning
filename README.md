# Merging Multiple DataFrame

If we have three tables we would like to merge together, we should see as follows

grant/ license/ ward

grants_licenses_ward = grants.merge(licenses, on=['address', 'zip'] \
                              .merge(wards, on='ward', suffixes=('_bus', '_ward'))
grants_licenses_ward.head()
