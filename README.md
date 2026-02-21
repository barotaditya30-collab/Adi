

using System;
using System.Text.RegularExpressions;

namespace ContactForm
{
    public partial class Default : System.Web.UI.Page
    {
        protected void BtnSubmit_Click(object sender, EventArgs e)
        {
            string name = txtName.Text.Trim();
            string email = txtEmail.Text.Trim();
            string phone = txtPhone.Text.Trim();

            // Name Validation
            if (string.IsNullOrEmpty(name))
            {
                lblMessage.ForeColor = System.Drawing.Color.Red;
                lblMessage.Text = "Please enter your name!";
                return;
            }

            // Email Validation
            if (!Regex.IsMatch(email, @"^[^@\s]+@[^@\s]+\.[^@\s]+$"))
            {
                lblMessage.ForeColor = System.Drawing.Color.Red;
                lblMessage.Text = "Please enter valid email!";
                return;
            }

            // Phone Validation (Only Numbers)
            if (!Regex.IsMatch(phone, @"^\d+$"))
            {
                lblMessage.ForeColor = System.Drawing.Color.Red;
                lblMessage.Text = "Phone number must contain only digits!";
                return;
            }

            // Success Message
            lblMessage.ForeColor = System.Drawing.Color.Green;
            lblMessage.Text = "Form Submitted Successfully!";
        }
    }
}
