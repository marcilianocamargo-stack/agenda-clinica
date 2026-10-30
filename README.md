Agenda Clínica
==============

Agenda de sessões, pacientes e financeiro (PWA). Os dados ficam salvos no próprio aparelho (localStorage).

## Backup

Toque no cabeçalho do app (Meu perfil) e depois em "Backup dos dados". Dá para salvar um arquivo ou copiar o texto, e restaurar por arquivo ou colando o texto.

## Trazer os dados do app antigo

O app antigo não tem o botão de backup, então use este atalho (bookmarklet) com o app antigo aberto no navegador. Ele copia os pacientes e sessões:

```
javascript:(function(){var d=JSON.stringify({app:"agenda-clinica",patients:JSON.parse(localStorage.ac_patients||"[]"),sessions:JSON.parse(localStorage.ac_sessions||"[]")});navigator.clipboard.writeText(d).then(function(){alert("Backup copiado! Abra o app novo e cole em Meu perfil > Backup dos dados.")},function(){prompt("Copie este texto:",d)})})();
```

No app novo: Meu perfil > Backup dos dados > colar no campo > "Colar backup".
