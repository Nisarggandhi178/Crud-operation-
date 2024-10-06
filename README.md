# Crud-operation-

SqlConnection con = new SqlConnection("DataSource ROWSHAN-PC;Initial Catalog ProgrammingDB;User ID=sa;Password=ro2229");
protected void Button1_Click(object sender, EventArgs e){
con.Open();
SqlCommand comm = new
SqlCommand("Insert into StudentInfo_Tab
values("+int.Parse(TextBox1.Text) +","+TextBox2.Text+","+DropDownList1.Sele ctedValue+","+double.Parse(TextBox3.Text) +","+TextBox4.Text+")", con); comm.ExecuteNonQuery(); con.Close(); ScriptManager.RegisterStartupScript(this,this.GetType(), "script", "alert('Successfully Inserted');",true);
LoadRecord();
}
void LoadRecord()
{
SqlCommand comm = new SqlCommand("select * from StudentInfo_Tab", con);
SqlDataAdapter d = new SqlDataAdapter(comm);
DataTable dt = new DataTable();
d.Fill(dt);
GridView1.DataSource = dt;
GridView1.DataBind();
}



{
con.Open();
SqlCommand comm
new SqlCommand("select from Student Info Tab where Student 10-)
SqlDataReader r = comm.ExecuteReader();
while (r.Read()){
TextBox2.Text=r.getvalue(3).ToString();
}
}
