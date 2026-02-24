using System.Data.SqlClient;
using System.Configuration;

protected void btnSubmit_Click(object sender, EventArgs e)
{
    string cs = ConfigurationManager.ConnectionStrings["con"].ConnectionString;

    using (SqlConnection con = new SqlConnection(cs))
    {
        string query = "INSERT INTO ContactForm (Name, Email, Phone, Address, IdentityNumber) VALUES (@Name, @Email, @Phone, @Address, @IdentityNumber)";

        SqlCommand cmd = new SqlCommand(query, con);
        cmd.Parameters.AddWithValue("@Name", txtName.Text);
        cmd.Parameters.AddWithValue("@Email", txtEmail.Text);
        cmd.Parameters.AddWithValue("@Phone", txtPhone.Text);
        cmd.Parameters.AddWithValue("@Address", txtAddress.Text);
        cmd.Parameters.AddWithValue("@IdentityNumber", txtIdentityNumber.Text);

        con.Open();
        cmd.ExecuteNonQuery();
        con.Close();
    }

    Response.Write("<script>alert('Form Submitted Successfully!');</script>");
}
