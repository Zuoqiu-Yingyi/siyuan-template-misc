.action{$blocks := (queryBlocks "SELECT * FROM blocks WHERE type='d' AND id ='?'" .id)}
.action{$name := ""}
.action{$memo := ""}
.action{$hpath := ""}
.action{$created := ""}
.action{$updated := ""}
.action{range $i, $v := $blocks}
    .action{$name = $v.Name}
    .action{$memo = $v.Memo}
    .action{$hpath = $v.HPath}
    .action{$created = $v.Created}
    .action{$updated = $v.Updated}
.action{end}

.action{$Title := ((((((((((((((((((((((((((((((((.title | replace "\\" "\\\\" ) | replace "`" "\\`" ) | replace "-" "\\-" ) | replace "=" "\\=" ) | replace "[" "\\[" ) | replace "]" "\\]" ) | replace ";" "\\;" ) | replace "'" "\\'" ) | replace "," "\\," ) | replace "." "\\." ) | replace "/" "\\/" ) | replace "~" "\\~" ) | replace "!" "\\!" ) | replace "@" "\\@" ) | replace "#" "\\#" ) | replace "$" "\\$" ) | replace "%" "\\%" ) | replace "^" "\\^" ) | replace "&" "\\&" ) | replace "*" "\\*" ) | replace "(" "\\(" ) | replace ")" "\\)" ) | replace "_" "\\_" ) | replace "+" "\\+" ) | replace "{" "\\{" ) | replace "}" "\\}" ) | replace "|" "\\|" ) | replace ":" "\\:" ) | replace "\"" "\\\"" ) | replace "<" "\\<" ) | replace ">" "\\>" ) | replace "?" "\\?" ) }
.action{$Name := (((((((((((((((((((((((((((((((($name | replace "\\" "\\\\" ) | replace "`" "\\`" ) | replace "-" "\\-" ) | replace "=" "\\=" ) | replace "[" "\\[" ) | replace "]" "\\]" ) | replace ";" "\\;" ) | replace "'" "\\'" ) | replace "," "\\," ) | replace "." "\\." ) | replace "/" "\\/" ) | replace "~" "\\~" ) | replace "!" "\\!" ) | replace "@" "\\@" ) | replace "#" "\\#" ) | replace "$" "\\$" ) | replace "%" "\\%" ) | replace "^" "\\^" ) | replace "&" "\\&" ) | replace "*" "\\*" ) | replace "(" "\\(" ) | replace ")" "\\)" ) | replace "_" "\\_" ) | replace "+" "\\+" ) | replace "{" "\\{" ) | replace "}" "\\}" ) | replace "|" "\\|" ) | replace ":" "\\:" ) | replace "\"" "\\\"" ) | replace "<" "\\<" ) | replace ">" "\\>" ) | replace "?" "\\?" ) }
.action{$Alias := ((((((((((((((((((((((((((((((((.alias | replace "\\" "\\\\" ) | replace "`" "\\`" ) | replace "-" "\\-" ) | replace "=" "\\=" ) | replace "[" "\\[" ) | replace "]" "\\]" ) | replace ";" "\\;" ) | replace "'" "\\'" ) | replace "." "\\." ) | replace "/" "\\/" ) | replace "~" "\\~" ) | replace "!" "\\!" ) | replace "@" "\\@" ) | replace "#" "\\#" ) | replace "$" "\\$" ) | replace "%" "\\%" ) | replace "^" "\\^" ) | replace "&" "\\&" ) | replace "*" "\\*" ) | replace "(" "\\(" ) | replace ")" "\\)" ) | replace "_" "\\_" ) | replace "+" "\\+" ) | replace "{" "\\{" ) | replace "}" "\\}" ) | replace "|" "\\|" ) | replace ":" "\\:" ) | replace "\"" "\\\"" ) | replace "<" "\\<" ) | replace ">" "\\>" ) | replace "?" "\\?" ) | replace "," "<br />")}
.action{$Memo := ((((((((((((((((((((((((((((((((($memo | replace "\\" "\\\\" ) | replace "`" "\\`" ) | replace "-" "\\-" ) | replace "=" "\\=" ) | replace "[" "\\[" ) | replace "]" "\\]" ) | replace ";" "\\;" ) | replace "'" "\\'" ) | replace "," "\\," ) | replace "." "\\." ) | replace "/" "\\/" ) | replace "~" "\\~" ) | replace "!" "\\!" ) | replace "@" "\\@" ) | replace "#" "\\#" ) | replace "$" "\\$" ) | replace "%" "\\%" ) | replace "^" "\\^" ) | replace "&" "\\&" ) | replace "*" "\\*" ) | replace "(" "\\(" ) | replace ")" "\\)" ) | replace "_" "\\_" ) | replace "+" "\\+" ) | replace "{" "\\{" ) | replace "}" "\\}" ) | replace "|" "\\|" ) | replace ":" "\\:" ) | replace "\"" "\\\"" ) | replace "<" "\\<" ) | replace ">" "\\>" ) | replace "?" "\\?" ) | replace "\n" "<br />")}

.action{$Hpath := (((((((((((((((((((((((((((((((($hpath | replace "\\" "\\\\" ) | replace "`" "\\`" ) | replace "-" "\\-" ) | replace "=" "\\=" ) | replace "[" "\\[" ) | replace "]" "\\]" ) | replace ";" "\\;" ) | replace "'" "\\'" ) | replace "," "\\," ) | replace "." "\\." ) | replace "/" "\\/" ) | replace "~" "\\~" ) | replace "!" "\\!" ) | replace "@" "\\@" ) | replace "#" "\\#" ) | replace "$" "\\$" ) | replace "%" "\\%" ) | replace "^" "\\^" ) | replace "&" "\\&" ) | replace "*" "\\*" ) | replace "(" "\\(" ) | replace ")" "\\)" ) | replace "_" "\\_" ) | replace "+" "\\+" ) | replace "{" "\\{" ) | replace "}" "\\}" ) | replace "|" "\\|" ) | replace ":" "\\:" ) | replace "\"" "\\\"" ) | replace "<" "\\<" ) | replace ">" "\\>" ) | replace "?" "\\?" ) }
.action{$Created := toDate "20060102150405" $created | date "2006-01-02 15:04:05"}
.action{$Updated := toDate "20060102150405" $updated | date "2006-01-02 15:04:05"}

| TITLE | .action{$Title} |   ID   | .action{.id}      |
| :---: | :-------------- | :----: | :---------------- |
| NAME  | .action{$Name}  |  PATH  | .action{$Hpath}   |
| ALIAS | .action{$Alias} | CTEATE | .action{$Created} |
| MEMO  | .action{$Memo}  | UPDATE | .action{$Updated} |
