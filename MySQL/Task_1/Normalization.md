Data sometimes is not clean or is denormalized, so we use normalization to organize it
1-first normal form:
When: table contains multivalued attribute(phone numbers).
Solution: by separating phone number into a new table and the primary key of student table will be set
as a foreign key in the new table.
2-2NF:
When:there are attributes that depends on some of keys not all.
Solution: create a new table and put the attributes that are partial dependency and make that part of
the key the primary key of the new table.
3-3NF:
When:non key attribute depends on non key attribute.
Solution:
Create new table and then move these attributes