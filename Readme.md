# Currency Apps
Aplikasi ini mencakup  fungsi perhitungan nilai tukar rupiah. Satu rupiah dianggap senilai Rp 15.000

## Scope & Functionalities
 - User dapat memasukkan angka
 - User dapat menyentuh tombol hitung
 - User mendapat info "INVALID" jika yang dimasukkan berupa text

## How does it works?

Diawali dari method `MainWindow` pada class MainWindow.xaml.cs

```csharp
       public MainWindow()
        {
            InitializeComponent();
            currency = new CurrencyController();
        }
```
logika perhitungan terdapat pada class `CurrencyController.cs` sebagai 
berikut cara kerjanya
```csharp
       public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```