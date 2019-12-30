---
layout: post
title: Use-Pdfium-rendering-engine | Windows Forms | Syncfusion
description: use Pdfium rendering engine
platform: windowsforms
control: PDF Viewer
documentation: ug
---

## Use Pdfium rendering engine

From Essential Studio 16.1.0.24 PDF viewer control provides a robust rendering of PDF document using Pdfium rendering engine. Please follow the below steps to use Pdfium PDF rendering in Syncfusion PDF viewer.

1.	Copy the Pdfium assembly&#39;s folder to a local folder from the installation path. The folder name must be &#34;Pdfium&#34;.

	The Pdfium assemblies will be available in 
    {$SystemDrive}:\Program Files (x86)\Syncfusion\Essential Studio\{Essential Studio version}\Pdfium 
	
	![](Use-Pdfium-rendering-engine_images/Use-Pdfium-rendering-engine_img1.png)
	
	N> The Pdfium folder will contain two folders namely x86 and x64, both would contain pdfium.dll assembly for the respective architecture. The Syncfusion PDF viewer is designed to detect the architecture of the target machine in which it is deployed and would pick corresponding pdfium.dll to use it. 
	
	![](Use-Pdfium-rendering-engine_images/Use-Pdfium-rendering-engine_img2.png)
	
2.	Then, the ReferencePath property of the PDF Viewer should be set to locate the &#34;Pdfium&#34; folder. 

	The following code snippet illustrates the same, you can also find the project sample in the below link. Here the &#34;Pdfium&#34; folder is placed inside the D:\ReferencePath\ folder.

{% tabs %}
{%highlight c#%}

	PdfViewerControl pdfViewerControl1 = new PdfViewerControl ();
	//Specify the path for Pdfium assembly. 
pdfViewerControl1.ReferencePath = @"D:\ReferencePath\";
	//Specify the PDF rendering engine as Pdfium.
	pdfViewerControl1.RenderingEngine =PdfRenderingEngine.Pdfium; 
	//Load the PDF document 
	pdfViewerControl1.Load("Sample.pdf");

{%endhighlight%}


{%highlight vb%}

	Dim pdfViewerControl1 As New PdfViewerControl()
    'Specify the path for Pdfium assembly
pdfViewerControl1.ReferencePath = @"D:\ReferencePath\"
    'Specify the PDF rendering engine as Pdfium
	pdfViewerControl1.RenderingEngine =PdfRenderingEngine.Pdfium 
	'Load the PDF document 
	pdfViewerControl1.Load("Sample.pdf")

{%endhighlight%}
{% endtabs %}

Please find the demo from the following link.

<http://www.syncfusion.com/downloads/support/directtrac/general/ze/WF-1752199577>