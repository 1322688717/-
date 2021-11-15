## 初次使用git配置以及git如何使用ssh密钥（将ssh密钥添加到github）

### 一、配置你的用户和邮箱

* 你需要运行命令来配置你的用户名和邮箱：

* $ git config --global user.name “liuhanxia”

* $ git config --global user.email "liuhanxia@51faguanggao.com"

* 注意：（引号内请输入你自己设置的名字，和你自己的邮箱）此用户名和邮箱是git提交代码时用来显示你身

* 份和联系方式的，并不是github用户名和邮箱


  ![在这里插入图片描述](https://img-blog.csdnimg.cn/20190610135036439.png)

### 二、生成你的ssh密钥

* 可以用 ssh-keygen 来创建。该程序在 Linux/Mac 系统上由 SSH 包提供，而在 Windows 上则包含在

  MSysGit 包里：

$ ssh-keygen -t rsa -C "your_email@youremail.com"
Creates a new ssh key using the provided email # Generating public/private rsa key pair.
Enter file in which to save the key (/home/you/.ssh/id_rsa):

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190610135453845.png)

* 直接按Enter就行。然后，会提示你输入密码，如下(建议输一个，安全一点，当然不输也行，应该不会有人闲的无聊冒充你去修改你的代码)：

![在这里插入图片描述](https://img-blog.csdnimg.cn/20190610135513790.png)

* Enter same passphrase again: [Type passphrase again]
  完了之后，大概是这样：



![在这里插入图片描述](https://img-blog.csdnimg.cn/20190610135523935.png)

### 三、查看你生成的公钥

* $ cat ~/.ssh/id_rsa.pub



![在这里插入图片描述](https://img-blog.csdnimg.cn/20190610135541668.png)

* 登陆你的github帐户。点击你的头像，然后 Settings -> 左栏点击 SSH and GPG keys -> 点击 New SSH key
* 然后你复制上面的公钥内容，粘贴进“Key”文本域内。 title域，自己随便起个名字。
* 点击 Add key。



### 四、整体流程

![image-20211115104933770](C:\Users\zcq\AppData\Roaming\Typora\typora-user-images\image-20211115104933770.png)