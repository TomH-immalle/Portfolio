# SoftwareOntwikkeling
***
## Portfolio
### 2017 CSharp
**ListBox met add en delete knop. De code:**
```
    public partial class MainWindow : Window
    {
        public MainWindow()
        {
            InitializeComponent();
        }



        private void addButton_Click(object sender, RoutedEventArgs e)
        {
            ListBoxItem newItem = new ListBoxItem();
            newItem.Content = textBox.Text;
            listBox.Items.Add(newItem);
            countTextBlock.Text = Convert.ToString("Aantal: "+listBox.Items.Count);
        }

        private void displayButton_Click(object sender, RoutedEventArgs e)
        {
            int index = Convert.ToInt32(indexTextBox.Text);
            ListBoxItem item = (ListBoxItem)listBox.Items[index];
            valueTextBox.Text = Convert.ToString(item.Content);
        }

        private void deleteButton_Click(object sender, RoutedEventArgs e)
        {
            var del = listBox.SelectedItem;
            if (del != null)
            {
                listBox.Items.Remove(del);
            }
            countTextBlock.Text = Convert.ToString("Aantal: " + listBox.Items.Count);
        }
    }
```
**Een programma dat ik voor Exercism heb gemaakt is Sum_Of_Multiples.**
**De code:**
```
 static void Main(string[] args)
        {
            Console.WriteLine("Give your numbers.");
            int x = Convert.ToInt16(Console.ReadLine());
            int y = Convert.ToInt16(Console.ReadLine());

            for (int i = x; i < 100; i+= x)
            {
                Console.WriteLine(i);
            }
            for (int i = y; i < 100; i+= y)
            {
                Console.WriteLine(i);
            }
        }
```
| Eerste repository | 
| ------ | 
| https://github.com/TomH-immalle/Balloon |

**Balloon is een programma dat ballonnen kan laten vergroten en laten stijgen.**
**De code:**
```
    public partial class MainWindow : Window
    {
        Ellipse ellip = new Ellipse();
        

        public MainWindow()
        {
            InitializeComponent();
            ellip.Width = 130;
            ellip.Height = 130;
            ellip.Margin = new Thickness(100, 100, 0, 0);
            ellip.Stroke = new SolidColorBrush(Colors.Red);
            canvas.Children.Add(ellip);
           
        }

        private void button_Click(object sender, RoutedEventArgs e)
        {
            ellip.Width = ellip.Width + 10;
            ellip.Height += 10;
        }

        private void button1_Click(object sender, RoutedEventArgs e)
        {
            
            ellip.Margin = new Thickness(ellip.Margin.Left, ellip.Margin.Top -10, ellip.Margin.Right, ellip.Margin.Bottom +10);
           
        }

        private void button2_Click(object sender, RoutedEventArgs e)
        {
            ellip.Width -= 10;
            ellip.Height -= 10;
        }

        private void button3_Click(object sender, RoutedEventArgs e)
        {
            ellip.Margin = new Thickness(ellip.Margin.Left, ellip.Margin.Top + 10, ellip.Margin.Right, ellip.Margin.Bottom - 10);
        }

        private void button4_Click(object sender, RoutedEventArgs e)
        {
            ellip.Width = 130;
            ellip.Height = 130;
            ellip.Margin = new Thickness(100, 100, 0, 0);
            ellip.Stroke = new SolidColorBrush(Colors.Red);
        }
    }
```
![C# cursus](https://image.ibb.co/evZ7dv/C_cursus.png)
****
**Student in Immaculata Instituut Oostmalle**
