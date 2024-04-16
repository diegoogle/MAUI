# MAUI
MAUI COURSE

## ¿Cómo funciona .NET MAUI?
.NET MAUI abstrae la implementación de un elemento de interfaz de usuario de su descripción lógica. Puedes describir la interfaz de usuario mediante XAML, un lenguaje neutro de plataforma basado en XML. Por ejemplo, el fragmento XAML siguiente muestra la descripción de un control de botón:

```
<Button Text="Click me"
        SemanticProperties.Hint="Counts the number of times you click"
        Clicked="OnCounterClicked"
        HorizontalOptions="Center" />
```

## Estructura del proyecto .NET MAUI e inicio de aplicaciones

- **App.xaml.** Este archivo define los recursos de la aplicación que la aplicación usará en el diseño XAML. Los recursos predeterminados se encuentran en la carpeta Resources y definen los colores para toda la aplicación y estilos predeterminados para cada control integrado de .NET MAUI.

- **App.xaml.cs.** Archivo de código subyacente para el archivo App.xaml. Este archivo define la clase App. Esta clase representa la aplicación en tiempo de ejecución. El constructor de esta clase crea una ventana inicial y le asigna la propiedadMainPage. Esta propiedad determina qué página se muestra cuando la aplicación comienza a ejecutarse.

- Eventos de ciclo de vida de aplicaciones:
    - OnStart
    - OnResume
    - OnSleep

- **AppShell.xaml.** Este archivo es una estructura principal de la aplicación de .NET MAUI. El Shell de .NET MAUI proporciona muchas características que son beneficiosas para aplicaciones de varias plataformas, entre las que se incluyen el estilo de las aplicaciones, la navegación basada en URI y las opciones de diseño, que incluyen la navegación flotante y las pestañas de la raíz de la aplicación.

- **MainPage.xaml.** Este archivo contiene la definición de la interfaz de usuario (etiquietas, botones, imagenes, etc).
También puede definir más páginas XAML si tiene una aplicación de varias páginas.

- **MainPage.xaml.cs.** Este es el código subyacente de la página. En este archivo se define la lógica para los distintos controladores de eventos y otras acciones desencadenadas por los controles de la página.

- **MauiProgram.cs.** Cada plataforma nativa tiene un punto de partida diferente que crea e inicializa la aplicación. Encontrará este código en la carpeta Plataformas del proyecto. Este código es específico de la plataforma, pero al final llama al método CreateMauiApp de la clase estática MauiProgram. 

- **Plataformas.** Esta carpeta contiene recursos y archivos de código de inicialización específicos de la plataforma. Hay carpetas para Android, iOS, MacCatalyst, Tizen y Windows.
Cuando se completa la inicialización, el código específico de la plataforma llama al método MauiProgram.CreateMauiApp que crea y ejecuta el objeto App