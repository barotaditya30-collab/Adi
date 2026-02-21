<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Default.aspx.cs" Inherits="ContactForm.Default" %>

<!DOCTYPE html>
<html>
<head runat="server">
    <title>Contact Form</title>

    <script type="text/javascript">
        function isNumberKey(evt) {
            var charCode = (evt.which) ? evt.which : evt.keyCode;
            if (charCode > 31 && (charCode < 48 || charCode > 57)) {
                return false;
            }
            return true;
        }
    </script>

</head>
<body>
    <form id="form1" runat="server">
        <div style="width:300px; margin:auto; margin-top:100px;">

            <h2>Contact Form</h2>

            Name:<br />
            <asp:TextBox ID="txtName" runat="server"></asp:TextBox>
            <br /><br />

            Email:<br />
            <asp:TextBox ID="txtEmail" runat="server"></asp:TextBox>
            <br /><br />

            Phone Number:<br />
            <asp:TextBox ID="txtPhone" runat="server" 
                onkeypress="return isNumberKey(event)">
            </asp:TextBox>
            <br /><br />

            <asp:Button ID="BtnSubmit" runat="server" 
                Text="Submit" 
                OnClick="BtnSubmit_Click" />
            <br /><br />

            <asp:Label ID="lblMessage" runat="server" 
                ForeColor="Green"></asp:Label>

        </div>
    </form>
</body>
</html>
