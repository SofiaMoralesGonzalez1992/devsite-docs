----[mlb]----

> WARNING
>
> Importante
>
> ¡Lo sentimos! Por el momento, esta página no se encuentra disponible en español.<br>
> [Ir a documentación en portugués](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/pt/guides/plugins/unofficial/vtex)

------------

----[mla]----

# VTEX

## ¿Qué es VTEX?

[VTEX](https://www.vtex.com/es/) es una **plataforma de e-commerce que permite recibir pagos con Mercado Pago.**

Puedes ofrecer a tus clientes la posibilidad de pagar con [tarjetas de crédito](#bookmark_condición_de_pagos_para_tarjeta_de_crédito), [tarjetas de débito](#bookmark_condición_de_pagos_para_tarjeta_de_débito) [medios de pago en efectivo](#bookmark_condición_de_pagos_para_medios_de_pago_en_efectivo). Como también, tienes la opción de [recibir pagos directamente desde el sitio web de Mercado Pago](#bookmark_condición_de_pagos_con_checkout_pro).


## Etapas para configurar

Los **pasos para comenzar a operar con Mercado Pago** son los siguientes:

1. Crea una [cuenta de vendedor](https://www.mercadopago[FAKER][URL][DOMAIN]/activities) en Mercado Pago si aún no tiene una.
2. Registra la afiliación con Mercado Pago.
3. Configura las condiciones de pago.
4. Agrega el device fingerprint.


## Configurar la afiliación de pasarela con Mercado Pago

Para crear una **afiliación de pasarela de pago con Mercado Pago**, sigue estos pasos:

1. Accede a las configuraciones del módulo en el panel de administración de tu tienda.
2. En la pestaña de Afiliación de Gateway, haz clic en el botón +.
3. Ingresa en el conector MercadoPagoV1.
4. Completa los campos correspondientes y guarda los cambios.

| Campos | Datos necesarios |
| --- | --- |
| Nombre de afiliación | Define el nombre que identificará a tu afiliación. |
| OAuth login | No es necesario. Dejar como está. |
| PublicKey | Refiere a las credenciales de tu cuenta de Mercado Pago. Completa con tu [clave pública]([FAKER][CREDENTIALS][URL]). |
| AccessToken | Refiere a las credenciales de tu cuenta de Mercado Pago. Completa con tu [clave privada]([FAKER][CREDENTIALS][URL]). |
| RefreshToken | Dejar en blanco. |
| ExpiredTokenIn | Dejar en blanco. |
| Merchant Account Id | Dejar en blanco. |
| Processing Mode | Elige `agregador` como modo de procesamiento a partir de MercadoPagoV1. |
| CountryName | Argentina. |
| Bill due date in days | Dejar en 1. |
| SoftDescriptor | Indica el nombre que va a aparecer para identificar una transacción de tu tienda en el resumen de la tarjeta del usuario. |
| Description | Escribe una breve descripción de tu negocio (opcional). |
| CategoryId | Elige la categoría de tus productos.|
| Financial Institution | Dejar en blanco. |
| External Installments | Elegir `Yes / Sí`. Usa las opciones de pago directamente de tu cuenta de Mercado Pago. |
| Antifraud | Elegir `Yes / Sí`. |
| Time Zone | Indica la región que define tu horario local. |
| Mercado Pago 3P payment due date | Deshabilitar. |
| 3P payment due date after Mercad Pago expiration | Deshabilitar. |
| MaxInstallments | Elige la cantidad de cuotas máximas que quieres ofrecer en Mercado Pago. |
| Categoria Principal | Selecciona la categoría correspondiente a su tienda. |
| Refund Method | Elige _Online refund if possible_ para hacer las devoluciones desde VTEX. Si las quieres desde Mercado Pago, deshabilitar. |
| Plan ahora 12 | Dejar en blanco. |
| Plan ahora 18 | Dejar en blanco. |
| Plan ahora 3 | Dejar en blanco. |
| Plan ahora 6 | Dejar en blanco. |
| Plan ahora Z | Dejar en blanco. |
| Charge Margine | Dejarlo en 0. |
| Binary Mode | Si se desea operar sin estados pendientes, activarlo. De caso contrario, dejarlo deshabilitado. |
| Enable pre-auth for GiftCards | Dejar desactivado. |
| Marketplace | Dejar en blanco. |
| Marketplace fee | Dejar en blanco. |
| Auto Settle | Dejar por defecto. |
| Early Security Capture | Puede desactivar la función o elegir en cuánto tiempo quieres realizar la captura (después de que se haya aprobado la transacción y se haya completado el análisis antifraude). |

![Imagen Afiliación](/images/vtex/vtex-hisp-afiliacion-arg.gif)


**¡Y listo! Tu afiliación con Mercado Pago ya se encuentra activa.**


## Configura las condiciones de pago

Luego de tener creada tu afiliación con MercadoPagoV2, puedes configurar pagos con[tarjetas de crédito](#bookmark_condición_de_pagos_para_tarjeta_de_crédito), [tarjetas de débito](#bookmark_condición_de_pagos_para_tarjeta_de_débito) o [medios de pago en efectivo](#bookmark_condición_de_pagos_para_medios_de_pago_en_efectivo). Como también, elegir la opción de [recibir pagos directamente en el Checkout Pro](#bookmark_condición_de_pagos_con_checkout_pro) y Checkout WB.


### Condición de pagos para el MercadoPagoPro

Para crear una condición de pago de MercadoPagoPro usando su afiliación con MercadoPagoV2, siga los pasos:

En el panel de administración, ingresa en Configuraciones de medios de pago.
En la pestaña Condiciones de pago, haz clic en +.
En la sección Otro, elige como condición de pago MercadoPagoPro.
Nombra la regla para ayudar facilitar la identificación y activa la condición en el campo Status.
En el campo Proceso con la afiliación, elige como afiliación a MercadoPagoV2.
Haz clic en Guardar.
¡Y listo! ¡Tu condición de pago de Checkout Pro Mercado Pago ya está activa!


Para poder utilizar este tipo de checkout se tienen que configurar los medios de pago por separado:

1. [Tarjetas de crédito](#bookmark_condición_de_pagos_para_tarjeta_de_crédito)
2. [Tarjetas de débito](#bookmark_condición_de_pagos_para_tarjeta_de_débito)
3. [Efectivo](#bookmark_condición_de_pagos_para_medios_de_pago_en_efectivo)
4. [Tarjetas de crédito locales](#bookmark_condición_de_pagos_con_medios_de_pagos_personalizados)


<br>

#### Condición de pagos para tarjeta de crédito

Para crear una condición de pagos con tarjeta de crédito, sigue estos pasos:

1. En el panel de administración, ingresa en Configuraciones de medios de pago.
2. En la pestaña Condiciones de pago, haz clic en +.
3. Luego, en la sección de Tarjetas de crédito, elige el medio de pago que quieras agregar. Se deben agregar Visa, MasterCard, American Express, Diners, Nativa, Naranja, Cabal y Shopping
4. Nombra la regla para ayudar facilitar la identificación y activa la condición en el campo Status.
5. En el campo Proceso con la afiliación, elige como afiliación a MercadoPagoV1.
6. En la opción de cuotas, selecciona cuotas automáticas. Esto te permite usar la configuración de tu cuenta de Mercado Pago.
7. Haz clic en Guardar.

> WARNING
>
> Importante
>
> Las cuotas deben quedar configuradas como automáticas para evitar problemas al procesar los pagos. Vamos a tomar las cuotas habilitadas en tu cuenta de Mercado Pago según corresponda. <br>


![Imagen tarjeta](/images/vtex/vtex-hispanos-credito.gif)


<br>

#### Condición de pagos para tarjeta de débito

Para crear una condición de pagos con tarjeta de débito, sigue estos pasos:

1. En el panel de administración, ingresa en Configuraciones de medios de pago.
2. En la pestaña Condiciones de pago, haz clic en +.
3. Luego, en la sección de Tarjetas de débito, elige el medio de pago que quieras agregar. Se deben agregar Visa débito, Master débito y Maestro.
4. Nombra la regla para ayudar facilitar la identificación y activa la condición en el campo Status.
5. En el campo Proceso con la afiliación, elige como afiliación a MercadoPagoV1.
6. En la opción de cuotas, selecciona cuotas automáticas. Esto te permite usar la configuración de tu cuenta de Mercado Pago.
7. Haz clic en Guardar.


<br>

#### Condición de pagos para medios de pago en efectivo

Para crear una condición de pago con medios de pago en efectivo, sigue estos pasos:

1. En el panel de administración, ingresa en Configuraciones de medios de pago.
2. En la pestaña Condiciones de pago, haz clic en +.
3. En la sección Factura, elige Boleto Bancario para agregar el medio de pago.
4. Nombra la regla para ayudar facilitar la identificación y activa la condición en el campo Status.
5. En el campo Proceso con la afiliación, elige como afiliación a MercadoPagoV1.
6. Haz clic en Guardar.

En VTEX, al seleccionar Boleto Bancario se incluyen todos los medios de pagos disponibles del país:

| Tipo de medio de pago | Medio de pago |
| --- | --- |
| `ticket` | Rapipago |
| `ticket` | Pago Fácil |
| `ticket` | Provincia NET Pagos |
| `atm` | Red Link |

> Los medios de pago Carga Virtual y Cobro Express no están disponibles para el Checkout de VTEX.


![Imagen efectivo](/images/vtex/vtex-hispanos-efectivo.gif)

<br>

#### Condición de pagos con medios de pagos personalizados

Los medios de pago personalizado permite sumar a VTEX tarjetas de crédito locales que VTEX no integra como una opción nativo y se pueden utilizar con Mercado Pago.

Para crear esta condición de pago, sigue estos pasos:

1. En el panel de administración, ingresa en Configuraciones de medios de pago.
2. En la pestaña Pagos personalizados, busca la sección Cobrands y haz clic en Configurar.
3. Se desplegará un formulario donde deberás ingresar Nombre, Descripción, Medio de pago (la marca bandera), Bines (validar en Mercado Pago los mismos) y el Código de Medio de Pago (es el nombre del medio de pago en Mercado Pago).
4. Haz clic en Guardar.
5. En la pestaña Planes de Pago, haz clic en +.
6. En la sección Pago personalizado, elige el medio de pago que habías creado para agregar el medio de pago.
7. Nombra la regla para ayudar facilitar la identificación y activa la condición en el campo Status.
8. En el campo Proceso con la afiliación, elige como afiliación a MercadoPagoV1.
9. Haz clic en Guardar.


> WARNING
>
> Importante
>
> Las cuotas deben quedar configuradas como automáticas para evitar problemas al procesar los pagos. Vamos a tomar las cuotas habilitadas en tu cuenta de Mercado Pago según corresponda. <br>

<br>
En VTEX, los medios de pago personalizados que se pueden agregar son:

| Tipo | Medio de pago | Bandera de la tarjeta | Bines | Código de pago del adquirente |
| --- | --- | --- | --- | --- |
| `credit_card` | Argencard | Mastercard | 501105-501105 | argencard |
| `credit_card` | Tarjeta Cencosud | Mastercard | 603493-603493 | cencosud |
| `credit_card` | Tarjeta CMR | Mastercard | 557039-557039 | cmr |
| `credit_card` | Tarjeta Cordial | Mastercard | 522135-522135,522137-522137,527555-527555 | cordial |
| `credit_card` | Tarjeta Cordobesa | Mastercard | 542702-542702,544764-544764,550073-550073,528824-528824 | cordobesa |
| `credit_card` | Tarjeta Mercado Pago Patagonia | Mastercard | 515073-515073,515070-515070,532383-532383,532384-532384 | mercadopago_cc |


![Imagen personalizado](/images/vtex/vtex-hisp-personalizado.gif)

------------


----[mlm]----

# VTEX

## ¿Qué es VTEX?

[VTEX](https://www.vtex.com/es/) es una **plataforma de e-commerce que permite recibir pagos con Mercado Pago.**

Puedes ofrecer a tus clientes la posibilidad de pagar con [tarjetas de crédito](#bookmark_condición_de_pagos_para_tarjeta_de_crédito),[tarjetas de débito](#bookmark_condición_de_pagos_para_tarjeta_de_débito) o [medios de pago en efectivo](#bookmark_condición_de_pagos_para_medios_de_pago_en_efectivo). Como también, tienes la opción de [recibir pagos directamente desde el sitio web de Mercado Pago](#bookmark_condición_de_pagos_con_checkout_pro).


## Etapas para configurar

Los **pasos para comenzar a operar con Mercado Pago** son los siguientes:

1. Crea una [cuenta de vendedor](https://www.mercadopago[FAKER][URL][DOMAIN]/activities) en Mercado Pago si aún no tiene una.
2. Registra la afiliación con Mercado Pago.
3. Configura las condiciones de pago.
4. Agrega el device fingerprint.


## Configurar la afiliación de pasarela con Mercado Pago

Para crear una **afiliación de pasarela de pago con Mercado Pago**, sigue estos pasos:

1. Accede a las configuraciones del módulo en el panel de administración de tu tienda.
2. En la pestaña de Afiliación de Gateway, haz clic en el botón +.
3. Ingresa en el conector MercadoPagoV1.
4. Completa los campos correspondientes y guarda los cambios.

| Campos | Datos necesarios |
| --- | --- |
| Nombre de afiliación | Define el nombre que identificará a tu afiliación. |
| OAuth login | No es necesario. Dejar como está. |
| PublicKey | Refiere a las credenciales de tu cuenta de Mercado Pago. Completa con tu [clave pública]([FAKER][CREDENTIALS][URL]). |
| AccessToken | Refiere a las credenciales de tu cuenta de Mercado Pago. Completa con tu [clave privada]([FAKER][CREDENTIALS][URL]). |
| RefreshToken | Dejar en blanco. |
| ExpiredTokenIn | Dejar en blanco. |
| Merchant Account Id | Dejar en blanco. |
| Processing Mode | Elige `agregador` como modo de procesamiento a partir de MercadoPagoV1. |
| CountryName | México. |
| Bill due date in days | Dejar en 1. |
| SoftDescriptor | Indica el nombre que va a aparecer para identificar una transacción de tu tienda en el resumen de la tarjeta del usuario. |
| Description | Escribe una breve descripción de tu negocio (opcional). |
| CategoryId | Elige la categoría de tus productos.|
| Financial Institution | Dejar en blanco. |
| External Installments | Elegir `Yes / Sí`. Usa las opciones de pago directamente de tu cuenta de Mercado Pago. |
| Antifraud | Elegir `No`. |
| Time Zone | Indica la región que define tu horario local. |
| Mercado Pago 3P payment due date | Deshabilitar. |
| 3P payment due date after Mercado Pago expiration. | Deshabilitar. |
| OrderExpirationHours | Elegir `1 hora`. Este campo define cada cuántas horas quieres que el sistema verifique el estado del pedido antes de que caduque. Si esta opción no se cumple, se configura al patrón de 192 horas.|
| MaxInstallments | Elige la cantidad de cuotas máximas que quieres ofrecer en Mercado Pago. |
| Categoria Principal | Selecciona la categoría correspondiente a su tienda. |
| Refund Method | Elige _Online refund if possible_ para hacer las devoluciones desde VTEX. Si las quieres desde Mercado Pago, deshabilitar. |
| Binary Mode | Si se desea operar sin estados pendientes, activarlo. De caso contrario, dejarlo deshabilitado. |
| Marketplace | Dejar en blanco. |
| Marketplace fee | Dejar en blanco. |
| Early Security Capture | Puede desactivar la función o elegir en cuánto tiempo desea realizar la captura (después de que se haya aprobado la transacción y se haya completado el análisis antifraude). |


> WARNING
>
> Importante
>
> En el campo Antifraud selecciona la opción `No` porque sino en el Checkout se le pedirá al pagador un identification para avanzar con el pago.
<br>


![Imagen Afiliación](/images/vtex/vtex-hisp-afiliacion.gif)


**¡Y listo! Tu afiliación con Mercado Pago ya se encuentra activa.**


## Configura las condiciones de pago
Luego de tener creada tu afiliación con MercadoPagoV2, puedes configurar pagos con [tarjetas de crédito](#bookmark_condición_de_pagos_para_tarjeta_de_crédito), [tarjetas de débito](#bookmark_condición_de_pagos_para_tarjeta_de_débito) o [medios de pago en efectivo](#bookmark_condición_de_pagos_para_medios_de_pago_en_efectivo). Como también, elegir la opción de [recibir pagos directamente en el Checkout Pro](#bookmark_condición_de_pagos_con_checkout_pro) y Checkout WB.

<br>

## Condición de pagos para el MercadoPagoPro

Para crear una condición de pago de MercadoPagoPro usando su afiliación con MercadoPagoV2, siga los pasos:

En el panel de administración, ingresa en Configuraciones de medios de pago.
En la pestaña Condiciones de pago, haz clic en +.
En la sección Otro, elige como condición de pago MercadoPagoPro.
Nombra la regla para ayudar facilitar la identificación y activa la condición en el campo Status.
En el campo Proceso con la afiliación, elige como afiliación a MercadoPagoV2.
Haz clic en Guardar.

**¡Y listo! ¡Tu condición de pago de Checkout Pro Mercado Pago ya está activa!**


<br>

## Condición de pagos para el MercadoPagoWallet

Para crear una condición de pago de MercadoPagoWallet usando su afiliación con MercadoPagoV2, siga los pasos:

En el panel de administración, ingresa en Configuraciones de medios de pago.
En la pestaña Condiciones de pago, haz clic en +.
En la sección Otro, elige como condición de pago MercadoPagoWallet.
Nombra la regla para ayudar facilitar la identificación y activa la condición en el campo Status.
En el campo Proceso con la afiliación, elige como afiliación a MercadoPagoV2.
Haz clic en Guardar.

**¡Y listo! ¡Tu condición de pago de Checkout WB Mercado Pago ya está activa!**

<br>

## Condición de pagos para el MercadoPagoOff

Para crear una condición de pago de MercadoPagoOff usando su afiliación con MercadoPagoV2, siga los pasos:

En el panel de administración, ingresa en Configuraciones de medios de pago.
En la pestaña Condiciones de pago, haz clic en +.
En la sección Otro, elige como condición de pago MercadoPagoOff.
Nombra la regla para ayudar facilitar la identificación y activa la condición en el campo Status.
En el campo Proceso con la afiliación, elige como afiliación a MercadoPagoV2.
Haz clic en Guardar.
**¡Y listo! ¡Tu condición de pago de Medios Off Mercado Pago ya está activa!**
