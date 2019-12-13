# ModernUI Theme for .Net WinForms

**ModernUI Theme** is a skin library that makes your .Net Windows Form Application look like ModernUI window in Win8/8.1 or Win10.

It redrews borders of stardard WinForm, and make a dropshadow around the window. You can set your form's border size and color, also you can set color of the dropshadow too.

![Screen Shot](http://ohtrip.cn/media/20180212015259.jpg)

## 2019/12/13 ##

.NET 4.6�Լ�֮��İ汾΢��ΪWinForm�����ԭ��������֧�֣���app.config�ļ��м���һ�´��뼴�ɿ���ԭ��������֧�֡�
```
<configuration>
    ...
    <System.Windows.Forms.ApplicationConfigurationSection>
        <add key="DpiAwareness" value="PerMonitorV2"/>
        <add key="EnableWindowsFormsHighDpiAutoResizing" value="true"/>
    </System.Windows.Forms.ApplicationConfigurationSection>
</configuration>
```
��Դ����ԣ��޸��˴���DPI�仯����Ϣ������ԭ���������´Σ����ⴰ�ڱ�����2�ε����⡣

## 2019/11/11 ���� ##

�����˶�Win8.1/Win10��PerMonitor/PerMonitorV2��DPI���API��֧��.

�����ܹ�ͨ�����dpiAwareness�����������Բ�ͬDPI�ӿڵ�֧�֡�

```
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <dpiAwareness xmlns="http://schemas.microsoft.com/SMI/2016/WindowsSettings">PerMonitorV2</dpiAwareness>
            <dpiAware xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">true</dpiAware>
        </windowsSettings>
    </application>
```

## 2019/11/2 ���� ##

����д�˴��ڵײ������������⣺

- �����С��֮�����ݴ���
- �������С��ʵ�ʴ�С��һ��
- ��ʼ�� WindowState ����Ϊ Maximized ʱ����λ�ô���
- FormBorderStyle����ΪNone��ȫ�����ڴ�С����ȷ
- Win7+ϵͳ�£���ק���ڵ����涥����󻯣���ԭʱ����λ�ô���

�޸ĵ�API

- ʹ��Borders���������BorderWidth���ԣ����ڿ���ʹ��Borders����[Padding����]��Ϊ����ָ��ÿ���߿�Ĵ�С
- ʹ��BorderColor���������ActiveBorderColor��InactiveBorderColor���ԣ�����ͳһʹ��BorderColor�������ñ߿���ɫ
- ʹ��ShadowColor���������ActiveShaodowColor��InactiveShadowColor���ԣ�����ͳһʹ��ShadowColor�������ô���ͶӰЧ��
- �Ƴ���BorderEffect���ԣ�����ֻ����DropShadowһ��ͶӰģʽ��ȡ����GlowͶӰ��ʽ��

 

## Features
- Make ModernUI-like Forms for .Net Windows Form Applications.
- Full window animations support (Not just set FormBorderStyle to None).
- Fast draw the dropshadow around the form.
- Support Form Active/Inactive state.

## NuGet
```
PM> Install-Package NetDimension.WinForm.ModernUI
```


## Example


```C#
	public partial class Form1 : ModernUIForm
	{
		public Form1()
		{
			InitializeComponent();
		}
	}
```

Change properties in "UI" category to make your form style as your wish.

## Donate

If you like my work, please buy me a cup of coffee to encourage me continue with this library. 
![Screen Shot](http://ohtrip.cn/media/beg_with_border.png)

[![DONATE](http://ohtrip.cn/media/PayPal-donate-button.png)](https://www.paypal.me/mrjson)