---
layout: post
title: CheckBoxAdv-Events | WindowsForms | Syncfusion
description: checkboxadv events
platform: WindowsForms
control: EditorsPackage
documentation: ug
---

# CheckBoxAdv Events

A detailed explanation about the CheckStateChanged event is given in the following section.

<table>
<tr>
<th>
CheckBoxAdv Events</th><th>
Description</th></tr>
<tr>
<td>
CheckStateChanged</td><td>
This event occurs when the CheckState property is changed.</td></tr>
<tr>
<td>
CheckedChanged</td><td>
This event is raised when the Checked property is changed.</td></tr>
</table>

## CheckStateChanged Event

This event occurs when the CheckState property is changed.

The event handler receives an argument of type EventArgs containing data related to this event.

{% tabs %}
{% highlight c# %}

private void checkBoxAdv1_CheckStateChanged(object sender, EventArgs e)
{
    Console.WriteLine(" CheckStateChanged event is raised");
}

{% endhighlight %}

{% highlight vb %}

Private Sub checkBoxAdv1_CheckStateChanged(ByVal sender As Object, ByVal e As EventArgs)
Console.WriteLine(" CheckStateChanged event is raised")
End Sub

{% endhighlight %}
{% endtabs %}

## CheckedChanged Event

This event is raised when the Checked property is changed. Checked property changes automatically when the CheckedState property is changed. Refer to the following code.

{% tabs %}
{% highlight c# %}

private void checkBoxAdv2_CheckedChanged(object sender, EventArgs e)
{
    if (!checkBoxAdv2.Checked)
        MessageBox.Show("Checkbox Unchecked");
    else
        MessageBox.Show("Checkbox checked");
}

{% endhighlight %}

{% highlight vb %}

Private Sub checkBoxAdv2_CheckedChanged(ByVal sender As Object, ByVal e As EventArgs)
If Not checkBoxAdv2.Checked Then
MessageBox.Show("Checkbox checked”)
Else
MessageBox.Show("Checkbox checked”)
End If
End Sub

{% endhighlight %}
{% endtabs %}