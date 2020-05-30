# 数据字典

Oracle通过数据字典来管理和展现数据库信息，数据字典通常储存数据库的元数据，是数据库的“数据库”。

1、数据字典里存有**用户信息**、用户的**权限信息**、所有**数据对象信息**、表的约束条件、统计分析数据库的结果等信息。

2、数据字典是学习、探索Oracle数据库原理的有力工具。

> |数据字典由数据字典基表 与 数据字典视图 构成。
>
> - 数据字典基表
>
>   表名一般以x$开头，由sys用户拥有
>
> - 数据字典视图
>
>   - 静态数据字典视图
>
>     表名一般以DBA_ USER_ ALL_ 开头，分别表示整个数据库的系统信息、当前用户拥有的对象信息、当前用户可以操作的对象信息。
>
>   - 动态数据字典视图
>
>     表名一般以v$开头，为了方便不同的用户查询，在创建数据库的时候，又生成了这些动态视图的同义词，所查询的动态视图其实是这些同义词。



```sql
desc dictionary
名称         空值 类型             
---------- -- -------------- 
TABLE_NAME    VARCHAR2(128)  
COMMENTS      VARCHAR2(4000)
```

## 数据字典视图

静态数据字典视图

```sql
select COUNT(*) from dba_views
where view_name like 'DBA_%'

select COUNT(*) from dba_views
where view_name like 'USER_%'

select COUNT(*) from dba_views
where view_name like 'ALL_%'
```

动态数据字典视图

```sql
select COUNT(*) from DBA_SYNONYMS
where SYNONYM_NAME like 'v$%'
```

