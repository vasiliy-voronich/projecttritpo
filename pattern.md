# “Одиночка” Singleton
 
Назначение: Гарантирует, что у класса есть только один экземпляр, и предоставляет  к нему  глобальную точку доступа. 
Пример: база данных может быть представлена только как один объект класса «DB»; должна быть только одна файловая система, один оконный менеджер и т.д. 
Другой пример: когда к объекту получают доступ различные части системы (например, календарь в Органайзере) 



## Возможные решения
 
Возможное решение – глобальная переменная – даёт доступ к объекту, но не запрещает создавать его экземпляры. 
Нужно, чтобы сам класс контролировал, что у него будет только один экземпляр. 
Применяем Singleton тогда, когда: 
-	должен быть только один экземпляр класса, доступный всем клиентам 
-	он должен быть легко доступен 
-	никто не может создать ещё один экземпляр 
-	он не должен быть создан, пока не требуется 


## Диаграмма классов

Для того, что бы Singleton было легко найти – храним его в поле класса, доступном через сообщение класса   чтобы он был только один – объявляем его со спецификатором private  	 для создания его в нужное  время – реализуем создание по требованию  
![](https://github.com/vasiliy-voronich/projecttritpo/blob/master/mockup/1.jpg)

## Пример кода

![](https://github.com/vasiliy-voronich/projecttritpo/blob/master/mockup/2.jpg) 
![](https://github.com/vasiliy-voronich/projecttritpo/blob/master/mockup/2.1.jpg)


**public class Calendar {  	private static Calendar instance;  	
private Calendar() {}  	public static getInstance(){
if (instance == null){ 
	 	instance = new Calendar();  
	 	 	} 
	 	return instance;} … }**
    
![](https://github.com/vasiliy-voronich/projecttritpo/blob/master/mockup/3.jpg)
![](https://github.com/vasiliy-voronich/projecttritpo/blob/master/mockup/4.jpg)
 
 ## Вариации
 
 Eager / Lazy инициализация 
  Thread Safe Singleton  
  Сериализуемый Singleton
 
![](https://github.com/vasiliy-voronich/projecttritpo/blob/master/mockup/5.jpg)




