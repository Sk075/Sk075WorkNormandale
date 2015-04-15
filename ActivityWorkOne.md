# Sk075WorkNormandale
Work Gitattribues

STORE
ST_ID			  INTEGER 			  NOT NULL,
ST_NAME			VARCHAR(30) 		NOT NULL,
ST_PHONE		CHAR(12)			  NOT NULL,
ST_CITY			VARCHAR(40) 		NOT NULL,
ST_STATE 	  VARCHAR(40)			NOT NULL,
PRIMARY KEY (ST_ID)); 

IVENTORY 
I_ID			  INTEGER 			NOT NULL,
ST_ID 			INTEGER				NOT NULL,
SU_ID 			INTEGER 			NOT NULL,
PRIMARY KEY (I_ID));
FOREIGN KEY (ST_ID) REFERENCES CLINIC ON STORE CASCADE);
FOREIGN KEY (SU_ID) REFERENCES CLINIC ON STORE CASCADE); 

SUPPLIERS 
SU_ID			INTEGER			NOT NULL,
SU_NAME			VARCHAR 		NOT NULL,
SU_QTY			SMALLIANT 		NOT NULL,
SU_PRB			NUMBER(9,3)		NOT NULL,
ST_CITY			VARCHAR(40) 	NOT NULL,
ST_STATE		VARCHAR(40)		NOT NULL,
ST_PHONE		CHAR			NOT NULL,
PRIMARY KEY (SU_ID));

CUSTOMERS 
CU_ID			INTEGER 			NOT NULL,
CU_FNAME		VARCHAR(35) 		NOT NULL,
CU_LNAME		VARCHAR(35) 		NOT NULL,
CU_PHONE		CHAR			NOT NULL,
CU_DOB			VARCHAR(40) 		NOT NULL,
CU_ADDRESS		VARCHAR(40)		NOT NULL,
CU_BALANCE 		NUMBER(9,3)		NOT NULL, 
PRIMARY KEY (CU_ID));

ORDER 
O_ID				INTEGER 			NOT NULL,
O_QTY			  SMALLIANT		  NOT NULL,
O_PRICE			NUMBER(9,3)		NOT NULL 
O_ITEMS			VARCHAR(40)		NOT NULL, 
CU_ID			  INTEGER 			NOT NULL, 
ST_ID			  INTEGER 			NOT NULL,
PRIMARY KEY (O_ID));
FOREIGN KEY (CU_ID) REFERENCES CLINIC ON STORE CASCADE);
FOREIGN KEY (ST_ID) REFERENCES CLINIC ON STORE CASCADE);

PRODUCT
P_ID				INTEGER 			NOT NULL, 
P_DESCRIPT 		CHAR(40)			NOT NULL,
P_DATE			DATE			NOT NULL
P_PRICE			NUMBER(9,3)		NOT NULL, 
CA_ID			INTEGER 			NOT NULL, 
O_ID				INTEGER 			NOT NULL, 
CU_ID  			INTEGER 			NOT NULL, 
PRIMARY KEY (P_ID));
FOREIGN KEY (CA_ID) REFERENCES CLINIC ON STORE CASCADE);
FOREIGN KEY (O_ID) REFERENCES CLINIC ON STORE CASCADE);
FOREIGN KEY (CU_ID) REFERENCES CLINIC ON STORE CASCADE);

CATEGORY 
CA_ID			INTEGER 			NOT NULL, 
CA_NAME			VARCHAR(26)		NOT NULL, 
CA_INFORMATION	CHAR(40)			NOT NULL,
CA_STATUS 		VARCHAR(18) 		NOT NULL, 
PRIMARY KEY (CA_ID));




























































































