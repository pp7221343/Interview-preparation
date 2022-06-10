# @Configuration注解和@Component
* 一样可以创建对象；@Configuration注解还可以让@Bean对象依赖于当前配置类的其它Bean

# @resource 和@autowired
* 都可以用来注入bean
* @Resource注解是Java自身的注解,@Autowired注解是Spring的注解
* @Resource注解有两个重要的属性,分别是name和type,如果name属性有值,则使用byName的自动注入策略,将值作为需要注入bean的名字,如果type有值,则使用byType自动注入策略,将值作为需要注入bean的类型.如果既不指定name也不指定type属性，这时将通过反射机制使用byName自动注入策略。即@Resource注解默认按照名称进行匹配,名称可以通过name属性进行指定，如果没有指定name属性，当注解写在字段上时，默认取字段名，按照名称查找,当找不到与名称匹配的bean时才按照类型进行装配。但是需要注意的是，如果name属性一旦指定，就只会按照名称进行装配
* @Autowired注解是spring的注解,此注解只根据type进行注入,不会去匹配name.但是如果只根据type无法辨别注入对象时,就需要配合使用@Qualifier注解或者@Primary注解使用. 
