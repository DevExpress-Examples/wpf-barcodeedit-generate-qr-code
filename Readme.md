<!-- default badges list -->
![](https://img.shields.io/endpoint?url=https://codecentral.devexpress.com/api/v1/VersionRange/128641935/24.2.1%2B)
[![](https://img.shields.io/badge/Open_in_DevExpress_Support_Center-FF7200?style=flat-square&logo=DevExpress&logoColor=white)](https://supportcenter.devexpress.com/ticket/details/T174016)
[![](https://img.shields.io/badge/📖_How_to_use_DevExpress_Examples-e9f6fc?style=flat-square)](https://docs.devexpress.com/GeneralInformation/403183)
[![](https://img.shields.io/badge/💬_Leave_Feedback-feecdd?style=flat-square)](#does-this-example-address-your-development-requirementsobjectives)
<!-- default badges end -->

# WPF BarCode Editor - Create a QR Code Generator

This example uses the [WPF BarCodeEdit](https://docs.devexpress.com/WPF/DevExpress.Xpf.Editors.BarCodeEdit) control to generate a QR code based on user input.

![WPF BarCodeEdit, DevExpress](https://raw.githubusercontent.com/DevExpress-Examples/how-to-create-a-qrcode-barcodecontrol-t174016/21.1.5%2B/i/wpf-barcode-editor-devexpress.png)

## Implementation Details

The `BarCodeEdit` control can display 27 types of barcodes. Use the [BarCodeEdit.StyleSettings](https://docs.devexpress.com/WPF/DevExpress.Xpf.Editors.BarCodeEdit.StyleSettings) property to specify the barcode type.

The Barcode editor's `EditValue` is bound to the `Text` property of the text box to automatically generate a QR code as the user types:

```xaml
<dxe:BarCodeEdit Grid.Row="0" AutoModule="True"
                    ShowText="False"
                    EditValue="{Binding Path=Text,ElementName=textBox}" >
    <dxe:BarCodeEdit.StyleSettings>
        <dxe:QRCodeStyleSettings CompactionMode="Byte" />
    </dxe:BarCodeEdit.StyleSettings>
</dxe:BarCodeEdit>
<TextBox Grid.Row="1" Name="textBox">
    DevExpress
</TextBox>
```

## Files to Review

* [MainWindow.xaml](./CS/BarCodeEdit/MainWindow.xaml) (VB: [MainWindow.xaml](./VB/BarCodeEdit/MainWindow.xaml))
<!-- feedback -->
## Does this example address your development requirements/objectives?

[<img src="https://www.devexpress.com/support/examples/i/yes-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=wpf-barcodeedit-generate-qr-code&~~~was_helpful=yes) [<img src="https://www.devexpress.com/support/examples/i/no-button.svg"/>](https://www.devexpress.com/support/examples/survey.xml?utm_source=github&utm_campaign=wpf-barcodeedit-generate-qr-code&~~~was_helpful=no)

(you will be redirected to DevExpress.com to submit your response)
<!-- feedback end -->
