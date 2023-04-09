### Описание работы JVM в данном классе
ClassLoader подгружает созданный класс в область памяти(Metaspace) подготавливает его и инициализирует.
При вызове создаётся фрейм main() в стеке(Stack Memory).

1. Во фрейме main() инициализируется пременная i и присваевается значение.
1. В куче(heap) создаётся объект(new Object),а ссылка на него(Object o) отправляется во фрейм main().
1. В куче создаётся объет ссылочного типа данных(Integer) ссылка на него передаётся в фрейм.
1. При вызове метода printAll() в стеке создаётся одноимённый фрейм куда записываются переданные в метод параметры,начинается выполнение написанного в методе кода.
1. В куче создаётся ссылочный тип данных(Integer),ссылка на него появляется в фрайме printAll(),присваевается значение.
1. Создётся новый фрейм в стеке куда передаётся ссылка на(o.toString(), i,  ii)
1. Создаётся еще один фрейм со ссылкой на("finished")

По мере заполнения памяти будет запускаться сборщик мусора,который проверяет достижимость ссылок и если они не достижимы удаляет,освобождая место в памяти.