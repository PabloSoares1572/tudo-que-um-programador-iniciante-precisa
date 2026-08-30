# Redes, HTTP e JSON

Uma rede envia dados entre programas. Na web, HTTP define requisições e respostas. Uma URL identifica recurso; DNS ajuda a converter nome em endereço; HTTPS protege comunicação em trânsito quando configurado corretamente.

JSON é formato textual comum de API. Ele não valida automaticamente seus dados: uma resposta pode ter campo ausente, tipo inesperado ou informação desatualizada.

Ao consumir API, defina timeout, verifique status, valide resposta e respeite autenticação/limites. Não registre header de autorização ou token em logs.

