# Source Control Systems
## PostGreSQL

1. Convert template db to ordinary db?

Ans: Append the following to bashsrc file:
```
UPDATE pg_database SET datistemplate='false' WHERE datname='election_ware_6_2_0_0';
```

2. Add column ot table?

Ans: Append the following to bashsrc file:
```
ALTER TABLE common.election
ADD COLUMN enable_risk_limiting_audit boolean DEFAULT false NOT NULL;
```