 恰当的变量名是可读性好的必要条件之一。特殊的变量如循环变量和状态变量要予以
特殊考虑。
· 命名约定可以区分局部、模块和全局变量。同时它还可以区分类型名称，比如可以对
命名常量、枚举类型和变量加以区分。
· 不管你从事的是哪种项目，都应该采用命名约定。所采用的命名约定取决于程序的规
模和从事这一程序的程序员的人数。
· 匈牙利约定是一种非常有效的命名约定，比较适于大规模项目和程序。
· 在现代编程语言中几乎不需要采用缩写技术。

用命名约定：

	1.	变量名称是否完全准确地描述了变量代表的是什么？
	•	示例：int totalStudents 比 int x 更能准确描述该变量代表学生总数。
	2.	变量名是否指向是客观世界中的问题，而不是关于这个问题的编程解决方案？
	•	示例：double interestRate（表示利率）比 double calcInterest（计算利率）更好，因为它指向了实际的利率，而不是计算过程。
	3.	变量名称是否足够长，使得你不必破译它？
	•	示例：String customerAddress 比 String addr 更容易理解。
	4.	变量名中如果含有计算限定词的话，是否将其放在最后？
	•	示例：int maxItemsCount 比 int countMaxItems 更好，因为限定词 Count 放在最后。
	5.	是否在名称中用 Count 或 Index 来代替了 Num？
	•	示例：int customerCount 比 int customerNum 更清晰表述它是一个计数。

对特殊类型数据的命名：

	1.	循环变量的名称是有意义的吗？
	•	示例：在嵌套循环中，for (int studentIndex = 0; studentIndex < totalStudents; studentIndex++) 比 for (int i = 0; i < totalStudents; i++) 更容易理解。
	2.	是否用更富于含义的名称来代替了临时变量？
	•	示例：String tempCustomerName 可以更换为 String previousCustomerName，这样表达更明确。
	3.	当逻辑变量的值是 True 时，它的名称是否充分表达了其含义？
	•	示例：boolean isValidPassword 比 boolean flag 更好，因为它表达了逻辑值的含义。
	4.	是否用前缀或后缀来表明了某些枚举类型是一类的？
	•	示例：enum Color { COLOR_RED, COLOR_GREEN, COLOR_BLUE } 比 enum Color { RED, GREEN, BLUE } 更加规范。
	5.	命名常量的名称是否是指向它们代表的实体而不是它们所代表的数值？
	•	示例：final int MAX_USER_COUNT = 100 比 final int HUNDRED = 100 更有意义，因为它表示具体的业务含义。

命名约定：

	1.	命名约定是否区分了局部、模块和全局数据？
	•	示例：局部变量使用小写驼峰命名，如 localVariable，全局常量使用大写蛇形命名，如 GLOBAL_CONSTANT。
	2.	命名约定是否对类型名称、命名常量、枚举类型和变量进行了区分？
	•	示例：类名使用大写驼峰命名法，如 CustomerService，常量使用全大写字母，如 MAX_RETRY_COUNT。
	3.	在不支持仅供子程序输入参数的语言中，命名约定是否对这类参数进行了标识？
	•	示例：可以通过添加 in 前缀来区分输入参数，如 void processOrder(inOrder order)，虽然 Java 一般不需要这样的区分。
	4.	命名约定是否与程序语言的标准约定尽可能地相容？
	•	示例：遵循 Java 的标准约定，如类名首字母大写，方法名和变量名使用小写驼峰式。
	5.	对于语言中没有强制的子程序中仅做输入的参数，是否约定将它标识了？
	•	示例：可以通过命名约定，如 final 关键字表示参数不会被修改。
	6.	是否对名称进行了格式化以增强程序的可读性？
	•	示例：List<String> customerNames 比 List<String>customerNames 更清晰。

短名称：

	1.	代码是否使用了长名称？
	•	示例：int productQuantity 比 int qty 更好，除非在明确上下文中。
	2.	是否避免了只省略一个字母的缩写？
	•	示例：int customerCount 比 int custCnt 更清晰。
	3.	所有单词保持缩写的连续性了吗？
	•	示例：int maxItemCount 比 int maxItemCnt 更一致。
	4.	所有的名称都是容易发音的吗？
	•	示例：customerTotal 比 custTot 更容易发音。
	5.	是否避免了会引起错误发音的名称？
	•	示例：userAccount 比 usrAcct 更易于发音且无混淆。
	6.	是否在注释表中对短变量名进行了注释？
	•	示例：如果必须使用短名称如 i，应在注释中解释 // i 表示索引。

避免如下常见的命名错误：

	1.	易引起误会的名称
	•	示例：list 可能令人误解为 List 类型，而实际上是一个数组，可以命名为 customerList。
	2.	含义相似的名称
	•	示例：避免将 studentCount 和 studentNumber 同时使用。
	3.	仅有一或两个字母不同的名称
	•	示例：dataProcessor 和 dataProcessors 容易混淆，建议采用不同的命名，如 dataHandler。
	4.	发音相似的名称
	•	示例：避免使用 userInput 和 userImport 这样的相似发音名称。
	5.	使用数字的名称
	•	示例：避免使用 int data1, data2，可以用 int firstData, secondData。
	6.	对单词作改写以使其比较短的名称
	•	示例：避免将 quantity 简化为 qty，尽量保持完整。
	7.	英语中常拼写错的名称
	•	示例：accommodation 比 accomodation 更准确，避免拼写错误。
	8.	标准库子程序或已定义的变量名又定义了
	•	示例：避免重新定义如 list 这样的标准库类名，改用 customList。
	9.	完全是随意的名称
	•	示例：避免使用无意义的名称如 tempData，而应使用有明确含义的 orderDetails。
	10.	含有难以辨识字母的名称
	•	示例：避免使用难以区分的字母如 l 和 1，可以改为 index。