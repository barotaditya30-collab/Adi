# Adi
Form
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Default.aspx.cs" Inherits="ContactForm.Default" %>

<!DOCTYPE html>
<html>
<head runat="server">
    <title>Simple Contact Form</title>
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
            border-radius: 10px;
            box-shadow: 0px 0px 10px gray;
        }
        .form-container input {
            width: 100%;
            padding: 8px;
            margin: 5px 0;
        }
        .btn {
            background-color: #0078D7;
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

            <asp:TextBox ID="txtName" runat="server" placeholder="Enter Name"></asp:TextBox>
            
            <asp:TextBox ID="txtPhone" runat="server" placeholder="Enter Phone Number"></asp:TextBox>
            
            <asp:TextBox ID="txtEmail" runat="server" placeholder="Enter Email ID"></asp:TextBox>
            
            <asp:Button ID="btnSubmit" runat="server" Text="Submit" CssClass="btn" OnClick="btnSubmit_Click" />
            
            <br /><br />
            
            <asp:Label ID="lblMessage" runat="server" ForeColor="Green"></asp:Label>
        </div>
    </form>
</body>
</html>
