# How to Add Prefix and Suffix to Axis Labels in a Syncfusion Blazor Chart

## Overview

This sample demonstrates how to customize axis label text in a Syncfusion [Blazor Charts](https://www.syncfusion.com/blazor-components/blazor-charts) by defining a custom `LabelFormat` value on the chart axis. The implementation formats numeric axis values with additional text before and after the generated value using the `${value}` placeholder pattern.

This approach is useful when chart data must be displayed with business-specific units, currency indicators, measurement suffixes, or shorthand notations while preserving automatic axis generation and scaling behavior.

## Key Features

- Uses the `SfChart` component from `Syncfusion.Blazor.Charts`.
- Configures `ChartPrimaryYAxis` with the `LabelFormat` property to inject custom text around axis values.
- Demonstrates the `${value}` placeholder syntax for axis label formatting.
- Uses `ChartRangePadding.Auto` on chart axes.
- Displays data with a `ChartSeries` configured using:
  - `DataSource`
  - `XName`
  - `YName`
  - `Type`
- Uses `ChartSeriesType.Column` to render the chart.
- Binds chart data through a `ChartData` model containing `XValue` and `YValue` properties.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone the repository.
2. Open Visual Studio 2022.
3. Select **Open a project or solution**.
4. Browse to the project file:
 
`CustomAxisLabel.csproj`
 
5. Restore NuGet packages if prompted.
6. Build the project.
7. Run the application using `Ctrl+F5`.

**Visual Studio Code**

1. Open the repository folder in Visual Studio Code.
2. Open the integrated terminal.
3. Navigate to the project directory that contains `CustomAxisLabel.csproj`.
4. Restore packages:

```bash
dotnet restore
```

5. Run the project:

```bash
dotnet run
```

6. Open the local application URL displayed in the terminal output.

## Project Structure

- `Pages/Index.razor` - Main sample page that renders the Syncfusion Blazor Chart (`SfChart`). Demonstrates custom axis label formatting using `ChartPrimaryYAxis.LabelFormat="${value}K"` to add a prefix and suffix around generated axis values.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Official documentation for chart axis customization and formatting: https://help.syncfusion.com/chart-sdk/blazor/charts/axis-customization

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.