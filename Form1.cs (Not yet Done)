namespace CalculatorApplication
{
    public partial class Form1 : Form
    {
        CalculatorClass cal;
        double num1, num2;
        string arithmetic;

        private void btnEqual_Click(object sender, EventArgs e)
        {
            num1 = Double.Parse(txtBoxInput1.Text);
            num2 = Double.Parse(txtBoxInput2.Text);
            arithmetic = cbOperator.Text;

            switch (arithmetic)
            {
                case "+":
                    cal.CalculateEvent += new Formula<double>(cal.GetSum);
                    lblDisplayTotal.Text = cal.GetSum(num1, num2).ToString();
                    cal.CalculateEvent -= new Formula<double>(cal.GetSum);
                    break;
                
                case "-":
                    cal.CalculateEvent += new Formula<double>(cal.GetDifference);
                    lblDisplayTotal.Text = cal.GetDifference(num1, num2).ToString();
                    cal.CalculateEvent -= new Formula<double>(cal.GetDifference);
                    break;
                
                case "*":
                    cal.CalculateEvent += new Formula<double>(cal.GetProduct);
                    lblDisplayTotal.Text = cal.GetProduct(num1, num2).ToString();
                    cal.CalculateEvent -= new Formula<double>(cal.GetProduct);
                    break;
                
                case "/":
                    cal.CalculateEvent += new Formula<double>(cal.GetQuotient);
                    lblDisplayTotal.Text = cal.GetQuotient(num1, num2).ToString();
                    cal.CalculateEvent -= new Formula<double>(cal.GetQuotient);
                    break;
                
                default:
                    lblDisplayTotal.Text = "Opps Error!";
                    break;
            }
        }

        public Form1()
        {
            InitializeComponent();
            cal = new CalculatorClass();
        }
    }
}
