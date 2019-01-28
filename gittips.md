## 解决Git log 中乱码的方法
```
git config --global core.quotepath false 

git config --global gui.encoding utf-8

git config --global i18n.commit.encoding utf-8 

git config --global i18n.logoutputencoding utf-8

#在Window中添加环境变量 
LESSCHARSET=utf-8

```
```mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->John: Hello John, how are you?
    loop Healthcheck
        John->John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail...
    John-->Alice: Great!
    John->Bob: How about you?
    Bob-->John: Jolly good!
```
