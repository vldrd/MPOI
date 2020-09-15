Лабораторна робота № 2. Функції lapply, sapply, split
================
В лабораторній роботі необхідно виконати наступні дії:


Завдання 1
----------

**Створити список list1 <- list(observationA = c(1:5, 7:3), observationB = matrix(1:6, nrow=2)). Для цього списку знайдіть sum за допомогою lapply.**

```{r}
list1 <- list(observationA = c(1:5, 7:3), observationB = matrix(1:6, nrow=2))
print(list1)

print(lapply(list1, sum))
```
**В:**
```{r}
##$observationA
##[1] 40

##$observationB
##[1] 21

```

Завдання 2
----------

**Для кожного елементу списку list1 знайдіть максимальне та мінімальне значення (range) за допомогою lapply та sapply.**

```{r}
lapply(list1, range)
sapply(list1, range)
```
**В:**
```{r}
##     observationA observationB
##[1,]            1            1
##[2,]            7            6
```

Завдання 3
----------

**Для вбудованого набору даних InsectSprays знайти середнє count для кожного spray.**

```{r}
grouped <- with(InsectSprays, split(count, spray))
print(sapply(grouped, mean))
```
**В:**
```{r}
##        A         B         C         D         E         F 
##14.500000 15.333333  2.083333  4.916667  3.500000 16.666667 
```