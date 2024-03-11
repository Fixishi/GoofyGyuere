# GoofyGyuere

# Stored XSS


1. Problém = Do disallowed_attributes jsem přidal onmouseover.
poté jsem ještě dodal href, style, src protože přes to se dá poslat JS
2. Problém = disallowed_attributes se dá jednoduše obejít tak že jakékoliv slova a keywords které jsou v tomto listu tím že ja napíšeme CAPS_LOCKEM myslím si že by bylo lepší udělat list která je nějak case insensitive

# Reflective XSS

Do SanitizeHtml jsem přidal s = html.escape(s) aby to escapnulo jakýkoli user input



# XSRF

Zde bych chtěl nejdříve změnit všechny GET na POST 

Poté je zde problém že pokud utočník dostane token může ho 24H používat. Proto jsem vytvořil funkci která dělá nová token např každou hodinu a poté druhou funkci která kontroluje jestli se daný token shoduje s tím co má uživatel.
