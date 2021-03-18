# vue-project

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).


## Заметки

### Создание компонента
1. Создать файл в папке components
2. Обязательная секция **template** с div внутри
3. import в род. компонент ```import ToDoList from '@/components/ToDoList.vue'```
4. Экспортируем компонент ```export default {}```
5. В родительском эл. внутри ```export default {}``` в поле **components** регистрируем компонент
*Сокращение default для emmet создает шаблон компонента*

### Данные
В родительском элементе создаем ```data() {return {}}```
- Внутри объекта мы можем создавать переменные, например массивы в виде *ключ*: *значение*
- Чтобы передать данные в шаблон используем директиву ```v-bind:todos='todos'```
- Чтобы компонент знал, что мы в него что-то передаем, в самом файле компонента в script вписываем ключ ```props:['todos']``` и передаем в массив название каждого элемента, который мы принимаем
- Чтобы итерировать данные из массива используем директиву ```v-for='todo of todos'``` в записи компонента в родительском элементе
- Используем ```v-bind:todo='todo'``` для передачи данных в шаблон
- Экспортируем в исходный компонент ```props:['todo']``` или в виде ключа *todo* с нужными нам параметрами
- v-on Позволяет регистрировать события. (@ - упрощенный синтакис)

### Router
- ```npm i vue-router``` - Установка роутера.
- В *SRC* создаем файл router.js
- Шаблон в роутере:
```
import Vue from 'vue';
import Router from 'vue-router';

Vue.use(Router);

export default new Router({
  mode: 'history',
  routes: [
    {
      path: '/',
      component: Home,
    },
  ],
});
```
- В *SRC* создаем папку views