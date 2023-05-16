```sql
SELECT
    *
FROM
    blocks AS b0
WHERE
    b0.id in (
        SELECT
            b1.id
        FROM
            blocks AS b1
        WHERE
            b1.markdown = '{{select * from blocks where id=''20060102030405-abcdefg''}}'
    )
```
{: custom-type="query-code" fold="1"}

<iframe src="/widgets/Query" data-src="/widgets/Query" data-subtype="widget" border="0" frameborder="no" framespacing="0" allowfullscreen="true" style="width: 8em; height: 2em; border: none; background-color: transparent;"></iframe>

{: custom-type="query-widget" custom-query-fields="['type', 'parent_id', 'hpath', 'created', 'updated',]"}
