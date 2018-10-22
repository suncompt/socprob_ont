# 社会課題のタグ付け

## 記述方法
tagannotate.ttlにRDF形式に基づいてデータを記述することでタグを追加できる．  
1つのRDFトリプルは「主語」「述語」「目的語」の三要素で構成され，それぞれをスペースで区切って記述する．
また，トリプルの最後には.をつける．
  
tag:1 rdf:type oa:Annotation .  
tag:1 oa:hasTarget <https://www.nikkei.com/article/DGXMZO24103660Q7A131C1CN8000/>.
tag:1 oa:hasBody sp:パワーハラスメント.
tag:1 oa:motivatedBy oa:tagging.
  
ただし，トリプルの最後の.の代わりに;を使用することで，次の行の「主語」を省略できる．
  
tag:1 rdf:type oa:Annotation ;  
  oa:hasTarget <https://www.nikkei.com/article/DGXMZO24103660Q7A131C1CN8000/>;  
  oa:hasBody sp:パワーハラスメント;  
  oa:motivatedBy oa:tagging.  
  
各述語の説明を以下に示す．

### rdf:type
主語がどのようなクラスであるかを示す．  
本データでは常に oa:Annotation を目的語に取る．

### oa:hasTarget
タグ付けのターゲットを示す．
<>でターゲットとなるURLを囲んだものを目的語に取る．

### oa:hasBody
付与するタグを示す．
タグ名の前にsp:をつけたものを目的語に取る．

### oa:motivatedBy
主語が何の目的で作られたものなのかを示す．
本データでは常に oa:tagging を目的語に取る．

