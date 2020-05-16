#面向接口编程
簡單理解编程时针对超类型（父类）进行编程，也就是说变量的声明类型（或方法的返回类型）是超类型，而不是具体的某个子类。

举例：動物園有若干動物，實現代碼帶線讓動物發聲
一.创建接口类`Animal.java`：

		public interface Animal {
			void makevoice();
		}

二. 创建实现类 `dog.java`:

		public class dog implements Animal {
		@Override
		public void makevoice() {
			System.out.println("汪汪汪。。。");
		}
	}		
1.針對實現編程的實現方法
	實現dog實例調用`makesound`方法
	
	Dog dog=new Dog();
	dog.make.makeSound();
2.針對接口編程的實現方法
	創建`heard_animalvoice.java`類
	
	public class heard_animalvoice {
		void heardvoice(Animal animal) {
		animal.makevoice();
		}
	}
	
通過接口調用

	heard_animalvoice ha=new heard_animalvoice();
	ha.heardvoice(new dog());
		
