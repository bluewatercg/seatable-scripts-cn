# Row

本文档将展示通过Base对象如何对行进行操作

如果您对Base对象还未了解，请参考

* [Base](base.md)

#### list rows

获取表格的所有行

```python
base.list_rows(table_name, view_name=None)
```

##### 例子

```python
rows = base.list_rows('Table1')
rows = base.list_rows('Table1', view_name='default')
```

#### append row

追加表格

```python
base.append_row(table_name, row_data)
```

##### 例子

```python
row_data = {
    "Name": "I am new Row"
}

base.append_row('Table1', row_data)
```

#### insert row

插入表格

```python
base.insert_row(table_name, row_data, anchor_row_id)
# anchor_row_id为锚定的行的id，将会把新行插入到这行下方
```

##### 例子

```python
row_data = {
    "Name": "I am new Row"
}

base.insert_row('Table1', row_data, 'U_eTV7mDSmSd-K2P535Wzw')
```

#### update row

更新一行

```python
base.update_row(table_name, row_id, row_data)
```

##### 例子

```python
row_data = {
    "dcXS": "123"
}
base.update_row('Table1', 'U_eTV7mDSmSd-K2P535Wzw', row_data)
```

#### delete row

删除一行

```python
base.delete_row(table_name, row_id)
```

##### 例子

```python
base.delete_row('Table1', 'U_eTV7mDSmSd-K2P535Wzw')
```

#### filter rows

过滤行

```python
base.filter_rows(table_name, filters, view_name=None, filter_conjunction='And')
```

##### 例子

```python
filters = [{
    "column_key":"0000",
    "filter_predicate":"contains",
    "filter_term":"a"
}],
base.filter_rows('Table1', filters=filters)
```