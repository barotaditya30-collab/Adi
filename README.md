CREATE TABLE ContactForm (
    Id INT PRIMARY KEY IDENTITY(1,1),
    Name NVARCHAR(100),
    Email NVARCHAR(100),
    Phone NVARCHAR(15),
    Address NVARCHAR(200),
    IdentityNumber NVARCHAR(50)
);
