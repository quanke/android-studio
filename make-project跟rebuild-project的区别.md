# Make Project跟Rebuild Project的区别

Make Project跟Rebuild Project都是执行相同的两个任务, 那他们的区别是什么?



最明显示的区别就是执行时间, 从上面的例子中我们可以看出,Make Project用时4.5秒,而Rebuild Project用时需要16秒.



为什么Rebuild Project会慢这么多？



因为Rebuild Project是对整个项目进行了重新编译,不管你之前有没有编译过,因此用时会比较长.



而Make Project只是对新产生变化的文件进行一次编译,已经编译过的文件就不用重编译了,所有用时比较少.

