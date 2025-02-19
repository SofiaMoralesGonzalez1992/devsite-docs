# ¿Qué es Suscripciones?

Las suscripciones de Mercado Pago te permiten recibir pagos de forma recurrente, con tarjeta de crédito y débito. La disponibilidad de los medios de pago varía según la forma de integración.

## Roles disponibles

Existen dos roles involucrados:
1. El __vendedor__ o __collector__, quien es dueño de la suscripción y acreedor de los importes que se debiten.
1. El __pagador__ o __payer__, quien abonará los importes de forma automática desde el medio de pago que haya elegido.

> NOTE
> 
> ¿Quieres crear suscripciones de forma rápida y simple?
> 
> Ingresa en la sección de [Suscripciones](https://www.mercadopago[FAKER][URL][DOMAIN]/subscription-plans) en el panel de tu cuenta de Mercado Pago, configura tus datos ¡y listo!


## Conceptos claves

Para poder integrar suscripciones, es necesario que conozcas cuatro conceptos claves:

| Concepto | Descripción |
| --- |	--- |
| Plan o template | Es una plantilla que permite definir, entre otros atributos, el título, monto y frecuencia de las suscripciones creadas por el vendedor. Sirve para establecer características generales en las suscripciones que se creen a partir de esta entidad. Es importante aclarar que aquí todavía no se configura ningún medio de pago.|
| Suscripción o preapproval | Autorización del pagador para cobros recurrentes con un medio de pago definido que va ser la base para crear cuotas según la recurrencia que se defina. Tiene características similares al template, ya que puede crearse una suscripción a partir de un plan. |
| Pago autorizado o authorized payment | Es la cuota de una suscripción que se genera y se cobra en base a la recurrencia definida. El motor de suscripciones calendariza y genera los pagos de forma automática. |
| Cobro de verificación | Se trata de un cobro mínimo, que se realiza en el momento de la adhesión del pagador solo para verificar que la tarjeta utilizada para pagar la suscripción es válida. Enseguida, este monto se reembolsa al pagador. |
| Fecha de facturación | Es la fecha que el vendedor puede establecer para recibir los cobros de una suscripción con una frecuencia de pago mensual. |


------------
### Próximos pasos
> LEFT_BUTTON_REQUIRED_ES
>
> Requisitos para integrar
>
> Revisa que esté todo bien en tu integración con los usuarios de prueba.
>
> [Requisitos para integrar](https://www.mercadopago[FAKER][URL][DOMAIN]/developers/es/guides/online-payments/subscriptions/previous-requirements)
