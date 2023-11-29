# How-to-add-prefix-and-suffix-for-axis-label-in-Blazor-chart

This article explains how to add prefix and suffix to the axis labels in Blazor chart.

**Adding prefix and suffix to the axis label in blazor column chart**

The [Blazor chart](https://www.syncfusion.com/blazor-components/blazor-charts) provides the support to format axis labels using global formatting options like 'N', 'C', and 'P' through the  [LabelFormat](https://help.syncfusion.com/cr/blazor/Syncfusion.Blazor.Charts.ChartAxis.html#Syncfusion_Blazor_Charts_ChartAxis_LabelFormat) property. Additionally, the axis supports the inclusion of prefixes and suffixes to the labels using placeholders such as ${value}K, where "value" represents the axis label, for instance, $20K. 

The following code illustrates the custom label formatting support for axis label in Blazor chart.

**C#**

```cshtml

@using Syncfusion.Blazor.Charts

<SfChart>

    <ChartPrimaryYAxis LabelFormat="${value}K" RangePadding="ChartRangePadding.Auto" />

    <ChartPrimaryXAxis RangePadding="ChartRangePadding.Auto" />

    <ChartSeriesCollection>
        <ChartSeries DataSource="@Data" XName="XValue" YName="YValue" Type="ChartSeriesType.Column" />
    </ChartSeriesCollection>

</SfChart>

@code {

    public class ChartData
    {
        public double XValue { get; set; }
        public double YValue { get; set; }
    }

    public List<ChartData> Data = new List<ChartData>
    {
        new ChartData { XValue = 10, YValue = 21 },
        new ChartData { XValue = 20, YValue = 24 },
        new ChartData { XValue = 30, YValue = 36 },
        new ChartData { XValue = 40, YValue = 38 },
        new ChartData { XValue = 50, YValue = 54 },
        new ChartData { XValue = 60, YValue = 57 },
        new ChartData { XValue = 70, YValue = 70 },
    };

}

```

The following screenshot illustrate the output of the above code snippet.

**Output**

![](/prefix-and-suffix-in-axis-label.png)

**Conclusion**

I hope you enjoyed learning how to add prefix and suffix for axis labels in Blazor Chart Component.

You can refer to our [Blazor Chart feature tour](https://www.syncfusion.com/blazor-components/blazor-charts) page to know about its other groundbreaking feature representations and [documentation](https://blazor.syncfusion.com/documentation/chart/getting-started), and how to quickly get started for configuration specifications. You can also explore our [Blazor Chart example](https://blazor.syncfusion.com/demos/chart/line?theme=bootstrap5) to understand how to create and manipulate data.

For current customers, you can check out our components from the [License and Downloads](https://www.syncfusion.com/sales/teamlicense) page. If you are new to Syncfusion, you can try our 30-day [free trial](https://www.syncfusion.com/downloads/blazor) to check out our other controls.

If you have any queries or require clarifications, please let us know in the comments section below. You can also contact us through our [support forums](https://www.syncfusion.com/forums), [support portal](https://support.syncfusion.com/create), or [feedback portal](https://www.syncfusion.com/feedback/blazor-components?control=charts). We are always happy to assist you!
