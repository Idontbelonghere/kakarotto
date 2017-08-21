## 基于程序分析技术的代码质量保障系统

通过静态扫描源程序,我们可以通过静态分析程序的语义计算出程序运行过程中可能出现的一些状态,从而自动检测出潜在的错误。

静态测试不需要我们实际运行所检测的软件系统,因而可以第一时间应用于软件开发过程中,在编码过程中发现并报告错误,将软件错误的危害和修复错误的代价降到最低。

Use [Wukong](https://jekyllrb.com/) to make your coding better.


### 为什么使用静态测试工具

软件代码质量问题是长期困扰软件业的重要问题之一。由于软件代码质量导致的bug会导致系统运行不稳定，并有可能引发严重的安全漏洞使得整个系统被恶意攻击，机密信息被窃取，形成不可估量的损失。目前软件的代码质量通常依赖人工复审和测试等手段来保障，存在费用高、效率低下、难于管理等问题。

基于程序分析技术的静态测试是业内认可的能够帮助保障软件质量的一种有效方法：通过静态扫描源程序，我们可以通过静态分析程序的语义计算出程序运行过程中可能出现的一些状态，从而自动检测出潜在的错误。静态测试不需要我们实际运行所检测的软件系统，因而可以第一时间应用于软件开发过程中，在编码过程中发现并报告错误，将软件错误的危害和修复错误的代价降到最低。

### 同类软件缺陷

一些先进的静态检测工具已经在业内广泛使用了，比如：
开源工具有UNO、Splint、Clang、FindBugs、infer等，
商业工具有KlockWork、Veracode、Polyspace、Fortify、Coverity等，
Facebook、微软、Oracle等也开发了此类工具在公司内部使用。
但这些工具都存在着误报率过高、运行时间过长、 不能有效检测深层次错误等问题。

最成功的商业工具Coverity自称误报率在10%-15%左右，但有公司评测其实际误报率通常达到60%-75%，而其他商业和开源工具的误报率更为严重；对于超过百万行的大型软件系统，这些商业软件通常需要超过一天的时间来分析，如Fortify在分析Java HotSpotVM（37 万行C++程序时耗时达到 5 天。在漏报方面，由于不确定系统内的已知错误的多少，因而我们无法给出一个准确量化的估计。但近年影响比较大的一些安全漏洞，如OpenSSL库中的 HeartBleeding漏洞，BashScript中的ShellShock漏洞，Android系统媒体库中的StageFright漏洞均没有由这些商业工具检测出。


### Wukong的优势

1. 能够有效发现已有工具无法检测到的深层次错误，特别是类似 HeartBleeding 漏洞等涉及复杂指针和别名关系的错误
2. 在误报率方面能够在已有工具上进一步提高，在找到更多错误的基础上避免引入更多的误报
3. 提供方便的接口可以通过用户描述定义新的错误类型
4. 分析效率方面能够在一分钟内分析上万行代码，适用于个人开发阶段在个人PC上进行检测

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Idontbelonghere/kakarotto/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
