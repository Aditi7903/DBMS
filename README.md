Project Phase 3: Relational Model
ER Diagram to Relational Model:

    Mapping of Strong Entity Types:
        Created relations for strong entities (STAFF, CANTEEN, ORDER, CUSTOMER, PAYMENT) including all simple attributes.
        Composite attributes were split into simple attributes to avoid 1-NF violation.

    Mapping of Weak Entity Types:
        Created relations for weak entities and included primary keys of owner entities as foreign keys. These keys, along with partial keys, form the primary key of the relation.
        Example: CanteenID in MENU ITEMS and CanteenID and CustomerID in FEEDBACK.

    Mapping of Binary 1:1 Relationship Types:
        No binary 1:1 relationship types in the ER model, so no changes were needed.

    Mapping of Binary 1
    Relationship Types:
        Included the primary key of the 1-side entity as a foreign key in the N-side entity's relation.
        Examples: CustomerID in PAYMENT, CanteenID in STAFF, SuperStaffID in STAFF.

    Mapping of Binary M
    Relationship Types:
        Created a new relation for each binary M
        relationship type, including primary keys of participating entities as foreign keys.
        Example: CONTAINS relation with OrderID, Iname, and Item quantity.

    Mapping of Multivalued Attributes:
        Created new relations for multivalued attributes, including the primary key of the entity type that has the attribute.
        Examples: INGREDIENTS and PHONE NUMBER.

    Mapping of N-ary Relationship Types:
        Created new relations for relationships of degree > 2, including primary keys of participating entities as foreign keys.
        Examples: SERVES with CanteenID, OrderID, CustomerID and PROVIDES with CustomerID, CanteenID, S.No.

Normalization:

    1-NF:
        The database is in 1-NF as there are no multivalued, composite, or nested attributes after mapping the ER diagram to the relational model.

    2-NF:
        The database is in 2-NF as every non-prime attribute is fully functionally dependent on the primary key.

    3-NF:
        To normalize the STAFF relation:
            Created a new table STAFF DETAILS with Aadhar as the primary key.
            Original STAFF table now references Aadhar from STAFF DETAILS.
