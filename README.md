# AmazonS3_Uploader_ASP.NET
Instructions=============

1. 
    Make appropriate MS SQL database/stored procedures.(for the name of the files).
        full querie shown below
    
2. 
    Use your secret/access keys.(You can see where it goes in the files)
3.  
    JS file shows how to use the serverside with React.
4.
    Enjoy
    
    Making the table/storedprocedure===========================

BEGIN

CREATE TABLE Uploads
(
ID int IDENTITY (1, 1) PRIMARY KEY NOT NULL,
DateCreated datetime2(7) NOT NULL,
URL nvarchar(1000) NOT NULL,
UserId int NOT NULL
)

END

BEGIN

CREATE PROC UploadsProc

@UserId int,
@URL nvarchar(1000)

AS

INSERT INTO Uploads(

UserId,
URL
)

VALUES (

@UserId,
@URL
)

END
