---
title: Contacta
subtitle: 'Tens dubtes si et puc ajudar?  Envia''m un missatge i en parlem'
published: false
form:
    name: contact
    fields:
        email:
            label: ''
            placeholder: 'Entra el teu correu electrònic'
            type: email
            validate:
                required: true
        message:
            lable: ''
            placeholder: 'Explica''m els teus dubtes!'
            type: textarea
            validate:
                required: true
        g-recaptcha-response:
            label: Captcha
            type: captcha
            recaptcha_not_validated: 'Captcha not valid!'
    buttons:
        submit:
            type: submit
            value: Enviar
        reset:
            type: reset
            value: Esborrar
    process:
        captcha: true
        save:
            fileprefix: contact-
            dateformat: Ymd-His-u
            extension: txt
            body: '{% include ''forms/data.txt.twig'' %}'
        email:
            subject: '[Missatge enviat a susannafort.cat] {{ form.value.name|e }}'
            body: '{% include ''forms/data.html.twig'' %}'
        message: 'Gràcies per contactar, et respondré el més aviat possible'
        display: thankyou
---

