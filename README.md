<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Default.aspx.cs" Inherits="ContactForm.Default" %>

<!DOCTYPE html>
<html>
<head runat="server">
    <title>Contact Form</title>
    <style>
        body {
            font-family: Arial;
            background-color: #f2f2f2;
        }
        .form-container {
            width: 300px;
            margin: 100px auto;
            padding: 20px;
            background: white;
            border-radius: 5px;
            box-shadow: 0px 0px 10px gray;
        }
        input {
            width: 100%;
            padding: 8px;
            margin: 8px 0;
        }
        .btn {
            background-color: #4CAF50;
            color: white;
            border: none;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <form id="form1" runat="server">
        <div class="form-container">
            <h2>Contact Form</h2>

            <asp:TextBox ID="txtName" runat="server" Placeholder="Enter Name"></asp:TextBox>

            <asp:TextBox ID="txtEmail" runat="server" Placeholder="Enter Email"></asp:TextBox>

            <asp:TextBox ID="txtPhone" runat="server" Placeholder="Enter Phone Number"></asp:TextBox>

            <asp:Button ID="btnSubmit" runat="server" Text="Submit" CssClass="btn" OnClick="btnSubmit_Click" />

        </div>
    </form>
</body>
</html>
