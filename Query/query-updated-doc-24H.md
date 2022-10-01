```sql
-- Query the documents updated within 24 hours.
SELECT
    '[' || b.content || '](siyuan://blocks/' || b.id || ')' AS __1____pre__doc_title,
    CASE
        WHEN b.updated != '' THEN b.updated
        ELSE b.created
    END AS __2____datetime__last_update_time,
    '[' || b.hpath || '](siyuan://blocks/' || b.id || ')' AS __3____pre__doc_path
FROM
    blocks AS b
WHERE
    b.type = 'd'
    AND b.root_id != '.block{.root_id}'
    AND (
        b.updated > strftime(
            '%Y%m%d%H%M%S',
            'now',
            'localtime',
            '-1 day'
        )
        OR b.created > strftime(
            '%Y%m%d%H%M%S',
            'now',
            'localtime',
            '-1 day'
        )
    )
ORDER BY
    __2____time__last_update_time DESC;
```
{: custom-type="query-code" fold="1"}

<iframe src="/widgets/Query" data-src="/widgets/Query" data-subtype="widget" border="0" frameborder="no" framespacing="0" allowfullscreen="true"></iframe>

{: custom-type="query-widget"}
