```sql
SELECT
    *
FROM
    blocks as b0
WHERE
    (
        b0.id IN (
            SELECT
                r1.block_id
            FROM
                refs as r1
            WHERE
                r1.def_block_id = '.root{.id}'
        )
        AND (
            b0.type = 'h'
            OR b0.type = 'p'
            OR b0.type = 't'
        )
        AND b0.parent_id NOT IN (
            SELECT
                b1.id
            FROM
                blocks as b1
            WHERE
                b1.type = 'i'
        )
    )
    OR (
        b0.id IN (
            SELECT
                b2.parent_id
            FROM
                blocks as b2
            WHERE
                b2.id IN (
                    SELECT
                        r2.block_id
                    FROM
                        refs as r2
                    WHERE
                        r2.def_block_id = '.root{.id}'
                )
        )
        AND b0.type = 'i'
    )
ORDER BY
    b0.updated DESC;
```
{: custom-type="query-code" fold="1"}

<iframe src="/widgets/Query" data-src="/widgets/Query" data-subtype="widget" border="0" frameborder="no" framespacing="0" allowfullscreen="true" style="width: 8em; height: 2em; border: none; background-color: transparent;"></iframe>

{: custom-type="query-widget" custom-query-fields="['type', 'content', 'ial', 'hpath', 'created', 'updated']"}
