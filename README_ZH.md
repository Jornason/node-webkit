## ����

node-webkit��һ������`Chromium`��`node.js`��Ӧ������ʱ. 
������node-webkit�����ʹ��HTML��Javascript����д����Ӧ��. 
ͬ��, ͨ�����������DOM��ֱ�ӵ���Node.js��ģ��, 
�����Ͳ�����һ�ֿ���ʹ�������Web��������д����Ӧ�õ�ȫ�·�ʽ.

��������Ӣ�ض���Դ��������.


[node-webkit����(�õ�Ƭ)](https://speakerdeck.com/u/zcbenz/p/node-webkit-app-runtime-based-on-chromium-and-node-dot-js)   
[ʹ��node-webkit��������Ӧ�ó���](http://strongloop.com/strongblog/creating-desktop-applications-with-node-webkit/)     
[ʹ��node-webkit��WebӦ��ת��Ϊ����Ӧ��(�õ�Ƭ)](http://oldgeeksguide.github.io/presentations/html5devconf2013/wtod.html)

## ����

* ʹ��HTML5, CSS3, JS �� WebGL ����дӦ��.
* ��ȫ��֧��[Node.js APIs](http://nodejs.org/api/) �������е� [��������](https://npmjs.org).
* ���ܸ�Ч: Node �� WebKit��ͬһ���߳�������: ��������ֱ�ӵ���; ������ͬһ������, ������ֱ���໥����;
* ��ݵĴ���ͷ���Ӧ��.
* ֧��Linux, Mac OSX �� Windows

## ����
[v0.9.2 ������־](https://groups.google.com/d/msg/node-webkit/qpBhcWr-hSc/caGjhtl8cEgJ)

Ԥ����������ļ� (v0.9.2 - 2014/2/20):

* Linux: [32λ](https://s3.amazonaws.com/node-webkit/v0.9.2/node-webkit-v0.9.2-linux-ia32.tar.gz) / [64λ] (https://s3.amazonaws.com/node-webkit/v0.9.2/node-webkit-v0.9.2-linux-x64.tar.gz)
* Windows: [win32](https://s3.amazonaws.com/node-webkit/v0.9.2/node-webkit-v0.9.2-win-ia32.zip)
* Mac: [32λ, 10.7+](https://s3.amazonaws.com/node-webkit/v0.9.2/node-webkit-v0.9.2-osx-ia32.zip)

**�����ı���Nodeģ��ֻ����Node v0.10������, �����ѡ�� node-webkit v0.8.x, ��Ҳ������ά����һ����֧. [������Ϣ](https://groups.google.com/d/msg/node-webkit/2OJ1cEMPLlA/09BvpTagSA0J)**  
[v0.8.5 ������־](https://groups.google.com/d/msg/node-webkit/Izwu5icHFOQ/0A-3uEKfldkJ)

Ԥ����������ļ� (v0.8.5 - 2014/2/26):

* Linux: [32λ](https://s3.amazonaws.com/node-webkit/v0.8.5/node-webkit-v0.8.5-linux-ia32.tar.gz) / [64λ] (https://s3.amazonaws.com/node-webkit/v0.8.5/node-webkit-v0.8.5-linux-x64.tar.gz)
* Windows: [win32](https://s3.amazonaws.com/node-webkit/v0.8.5/node-webkit-v0.8.5-win-ia32.zip)
* Mac: [32λ, 10.7+](https://s3.amazonaws.com/node-webkit/v0.8.5/node-webkit-v0.8.5-osx-ia32.zip)

[��ʷ�汾](https://github.com/rogerwang/node-webkit/wiki/Downloads-of-old-versions)

###ʾ������ʵӦ��
�����ͬ����[���ǵ�ʾ����](https://github.com/zcbenz/nw-sample-apps) and the [List of apps and companies using node-webkit](https://github.com/rogerwang/node-webkit/wiki/List-of-apps-and-companies-using-node-webkit)����Ȥ.


## ��������

���� `index.html`:

```html
<!DOCTYPE html>
<html>
  <head>
    <title>Hello World!</title>
  </head>
  <body>
    <h1>Hello World!</h1>
    We are using node.js <script>document.write(process.version)</script>.
  </body>
</html>
```

���� `package.json`:

```json
{
  "name": "nw-demo",
  "main": "index.html"
}
```

��`index.html`��`package.json`���һ��zip��, ����Ϊ`app.nw`:

````bash
$ zip app.nw index.html package.json
````

���������һ�������Ľṹ:

```
app.nw
|-- package.json
`-- index.html
```

�����ʺ������ϵͳ��node-webkit�汾, Ȼ��ʹ������`app.nw`�ļ�:

````bash
$ ./nw app.nw
````

ע��: Windows��, �����ͨ����`app.nw`ֱ����ק��`nw.exe`��������.

## �ĵ�

���˽���������α�д/���/����Ӧ��, �뿴:

* [�������Ӧ��](https://github.com/rogerwang/node-webkit/wiki/How-to-run-apps)
* [��δ���ͷ������Ӧ��](https://github.com/rogerwang/node-webkit/wiki/How-to-package-and-distribute-your-apps)
* [��node-webkit�����ʹ��Node.js��ģ��(��)](https://github.com/rogerwang/node-webkit/wiki/Using-Node-modules)

Ȼ��ͨ�����ǵ�[Wiki](https://github.com/rogerwang/node-webkit/wiki)�˽����.

## ����

����ʹ��[node-webkit group](http://groups.google.com/group/node-webkit)��Ϊ�ʼ��嵥 (ֻʹ��Ӣ��).
ͨ��[node-webkit+subscribe@googlegroups.com](mailto:node-webkit+subscribe@googlegroups.com)����.
������GitHub�ϸ���.

�������IRC�Ϻ���������, irc.freenode.net�ϵ�##node-webkit Ƶ��

## ���

`node-webkit`�Ĵ��������MIT���, ���Բ鿴���ǵ�`LICENSE`�ļ�. ���·��������ƵĻ�, �ο�[��δ���ͷ������Ӧ��](https://github.com/rogerwang/node-webkit/wiki/How-to-package-and-distribute-your-apps)
