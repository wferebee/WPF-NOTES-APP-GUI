using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;
using System.Data;
using System.Collections;

namespace WPF_NOTES_APP_GUI
{
    
    public partial class MainWindow : Window
    {

        DataTable table;
        

        public int RowIndex { get; }


        public MainWindow()
        {
            InitializeComponent();
        }

        private void MainWindow1_Load(object sender, RoutedEventArgs e)
        {
            table = new DataTable();
            table.Columns.Add("Title", typeof(String));
            table.Columns.Add("Messages", typeof(String));




            string[] arrray = new string[10];
            DataGridView1.ItemsSource = table.DefaultView;
            

        }

        private void btnNew_Click(object sender, RoutedEventArgs e)
        {
            txtTitle.Clear();
            txtMessage.Clear();
        }

        private void btnSave_Click(object sender, RoutedEventArgs e)
        {

            table.Rows.Add(txtTitle.Text, txtMessage.Text);
           
            

            txtTitle.Clear();
            txtMessage.Clear();
        }

        private void btnRead_Click(object sender, RoutedEventArgs e)
        {
           
            int index = DataGridView1.Items.IndexOf(DataGridView1.CurrentItem);

            if(index >= 0)
            {
                txtTitle.Text = table.Rows[index].ItemArray[0].ToString();
                txtMessage.Text = table.Rows[index].ItemArray[1].ToString();
            }

        }

        private void btnDelete_Click(object sender, RoutedEventArgs e)
        {
            int index = DataGridView1.Items.IndexOf(DataGridView1.CurrentItem);
            table.Rows[index + 1].Delete();
        }

    }
}
