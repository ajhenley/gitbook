###Autoincrement with Oracle

####Oracle doesn't include an autoincrement type...

Here's an example how to add a sequence in Oracle 11g. If you're working with Oracle 12 the process has been simplified though this will work as well. 

{%ace edit=true, lang='sql'%}
CREATE TABLE MYTABLE (
  ID NUMBER NOT NULL,
  NAME VARCHAR2(100)
  CONSTRAINT "PK1" PRIMARY KEY (ID)
);
{%endace%}

####You will need to create a sequence
{%ace edit=true, lang='sql'%}
CREATE SEQUENCE S_MYTABLE
START WITH 1
INCREMENT BY 1
CACHE 10;
{%endace%}

####And a trigger
{%ace edit=true, lang='sql'%}
CREATE OR REPLACE TRIGGER T_MYTABLE_ID
BEFORE INSERT
ON MYTABLE
REFERENCING NEW AS NEW
FOR EACH ROW
BEGIN
  if(:new.ID is null) then
  SELECT S_MYTABLE.nextval
  INTO :new.ID
  FROM dual;
  end if;
END;
{%endace%}

####Then run:
{%ace edit=true, lang='sql'%}
ALTER TRIGGER "T_MYTABLE_ID" ENABLE;
{%endace%}

Alternatively, you can create an identity column from the Edit Table dialog in SQL Developer. Select the Identity tab. Then select the trigger name and column.

Remember, if you create a sequence and then delete the table the sequence continues to exist. If you recreate the table you won't be able to recreate the sequence. If you use the existing sequence then the numbering will pick up where the old sequence left off.

