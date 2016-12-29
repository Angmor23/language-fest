# language-fest

Inline Javascript, params highlighting and snippets.

![Screenshot](https://api.monosnap.com/rpc/file/download?id=kCLtIQXgsyYa9fmsvZAgfoDGtJo7M0)

## snippets

### fest:template
```
<fest:template xmlns:fest="http://fest.mail.ru" context_name="json">
  ${1:<!-- code -->}
</fest:template>
```

### fest:text
```
<fest:text>
  "${1:Hello, World}"
</fest:text>
```

### fest:space
```
<fest:space/>
```

### fest:set
```
<fest:set name="${1:name}">
  ${2:<!-- code -->}
</fest:set>
```

### fest:get
```
<fest:get name="${1:name}">
  <fest:params>
    {
      mods: [],
      mix: [],
      attrs: {}
    }
  </fest:params>
</fest:get>
```

### fest:script
  ```
  <fest:script>
    ${1:// code}
  </fest:script>
  ```

### fest:value
```
<fest:value output="text">
  ${1:<!-- code -->}
</fest:value>
```

### fest:if
```
<fest:if test="${1:true}">
  ${2:<!-- code -->}
</fest:if>
```

### fest:choose
```
<fest:choose>
  <fest:when test="${1:1 === 1}">
    <fest:text>one</fest:text>
  </fest:when>

  <fest:otherwise>
    <fest:text>More than 2</fest:text>
  </fest:otherwise>
</fest:choose>
```

### fest:each
```
<fest:each iterate="${1:arr}" index="${2:i}" value="${3:item}">
  ${4:<!-- code -->}
</fest:each>
```

### fest:for
```
<fest:for iterate="${1:arr}" index="${2:i}" value="${3:item}">
  ${4:<!-- code -->}
</fest:for>
```

### fest:comment
```
  <fest:comment>${1:comment}</fest:comment>
```

### fest:params
```
<fest:params>
  {
    mods: [],
    mix: [],
    attrs: {}
  }
</fest:params>
```

### fest:param
```
<fest:param name="${1:html}">
  ${2:<!-- code -->}
</fest:param>
```


### fest:cdata
```
<![CDATA[
  <script>
    console.log(JSON.parse(]]><fest:value output="json">JSON.stringify(${1:item})</fest:value><![CDATA[));
  </script>
]]>
```

### fest:mergeTopParams
```
  fest._helpers.mergeTopParams({}, params)
```

### fest:mergeParams
```
  fest._helpers.mergeParams(true, {}, params)
```

### fest:mix
```
mix: ['${1:mix_name}'],
```

### fest:mods
```
mods: ['${1:mod_name}'],
```

### fest:attrs
```
attrs: {
  ${1:attr_name}: ${2:attr_value}
},
```
