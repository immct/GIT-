GIT，一个版本管理控制工具。

在工作中，你是否需要和别人开发同一项目不同部分的代码？在自己的项目中，是否需要需要修改某部分代码，而又不想删掉之前的版本因此保留了很多份代码，通过在文件名上用1.2.3.4或者新增的功能来区分？

来使用我的Git，实现版本的方便管理吧。

它在本地实现了一个版本库，只要你在代码文件夹下Git init，它就记住了你当前文件夹的状态，将其记载在隐藏文件夹.git下。并且在你想得知自己文件夹修改情况的时候为你提供信息Git status。告诉你哪儿修改了。

等等。那如何实现多版本管理呢？难道我每次打开关闭文件你都保存一次状态吗？那太浪费了，我也不想保存那么多没用的状态啊。哈哈，你git add的时候我才会保存状态，然后你还要提供说明（-m）然后，git会为这一次add生成一些信息，你可以保存这些信息，然后通过这些信息找到之前的版本。

最后就是提交了。git commit就行了。

怎么远程操作呢？你可以add remote origin地址 然后这个地址写到了.git里面，告诉git我可能从那里获取，也可能向那里发送。（通过.git/config查看）（可以是github,bitbucket,或者是你自己的方案）。然后用push 和 pull获取和发送。

设置一下git config --global user.name xx user.email  xx 用于为每个项目打上项目者的名字，在社区积累信用。当然还有 --local选项 更强一点但范围小（你懂），更弱的是--system.
提交的时候有一个有趣的错误。linux和win下换行符不同（Typora默认是Linux风格）。为了免去这个问题，要在config里加上core.safecrlf=false, 即git config --global core.safecrlf false

github是最大的远程托管方案。可以在github上create repo，然后push下来，也可以在本地创建，然后push到github，还可以两方都有，连接起来。。。。


