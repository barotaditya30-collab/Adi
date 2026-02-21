

using System;

namespace ContactForm
{
    public partial class Default : System.Web.UI.Page
    {
        protected void btnSubmit_Click(object sender, EventArgs e)
        {
            string name = txtName.Text;
            string phone = txtPhone.Text;
            string email = txtEmail.Text;

            lblMessage.Text = "Form Submitted Successfully!";
        }
    }
}
