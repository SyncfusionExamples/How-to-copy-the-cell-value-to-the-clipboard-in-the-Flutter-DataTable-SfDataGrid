# How to copy the cell value to the clipboard in the Flutter DataTable (SfDataGrid)?

In this article, we will show you how to copy the cell value to the clipboard in the [Flutter DataTable](https://www.syncfusion.com/flutter-widgets/flutter-datagrid).

Initialize the [SfDataGrid](https://pub.dev/documentation/syncfusion_flutter_datagrid/latest/datagrid/SfDataGrid-class.html) widget with all the necessary properties. You can copy the cell value of the DataGrid by using [SelectableText](https://api.flutter.dev/flutter/material/SelectableText-class.html). To do this, wrap the DataGrid cell's value as a child of the SelectableText widget. Then, drag or right-click the cell value to select it, and right-click the selected value to copy it to the clipboard.

```dart
class EmployeeDataSource extends DataGridSource {

…

  @override
  DataGridRowAdapter buildRow(DataGridRow row) {
    return DataGridRowAdapter(
        cells: row.getCells().map<Widget>((e) {
      return Container(
        alignment: Alignment.center,
        padding: const EdgeInsets.all(8.0),
        child: SelectableText(e.value.toString()),
      );
    }).toList());
  }
}
```
You can download the example from [GitHub](https://github.com/SyncfusionExamples/How-to-copy-the-cell-value-to-the-clipboard-in-the-Flutter-DataTable-SfDataGrid).