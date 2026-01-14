# Configuração DNS para GitHub Pages

## Domínio: fiderede-lda.com

### Opção A: Registos A (Recomendado para domínio raiz)

Adicione **4 registos A** no seu registador de domínio:

```
Tipo: A
Nome/Host: @ (ou deixe em branco, ou coloque o domínio raiz)
Valor/IP: 185.199.108.153
TTL: 3600 (ou Auto)

Tipo: A
Nome/Host: @
Valor/IP: 185.199.109.153
TTL: 3600

Tipo: A
Nome/Host: @
Valor/IP: 185.199.110.153
TTL: 3600

Tipo: A
Nome/Host: @
Valor/IP: 185.199.111.153
TTL: 3600
```

### Opção B: CNAME (Alternativa)

Se o seu registador não permitir múltiplos registos A, pode usar CNAME:

```
Tipo: CNAME
Nome/Host: @ (ou www)
Valor: carlosmco1922.github.io
TTL: 3600
```

**Nota:** Alguns registadores não permitem CNAME no domínio raiz (@), apenas em subdomínios.

## Instruções por Registador Comum

### GoDaddy
1. Aceda ao seu painel de controlo
2. Vá a "DNS Management" ou "Gerir DNS"
3. Adicione os 4 registos A conforme acima
4. Guarde as alterações

### Namecheap
1. Aceda ao painel de controlo
2. Vá a "Advanced DNS"
3. Adicione os registos A
4. Guarde

### PTisp / Registadores Portugueses
1. Aceda ao painel de controlo do domínio
2. Procure por "DNS" ou "Gestão DNS"
3. Adicione os registos A
4. Guarde

## Verificação

Após configurar o DNS:

1. **Aguarde 5-60 minutos** para a propagação DNS
2. No GitHub: Settings > Pages > Custom domain
3. Clique em **"Check again"**
4. Se estiver correto, o erro desaparecerá
5. Poderá então ativar **"Enforce HTTPS"**

## Verificar DNS Online

Pode verificar se os registos estão corretos usando:

- https://dnschecker.org/#A/fiderede-lda.com
- https://www.whatsmydns.net/#A/fiderede-lda.com

Procure pelos IPs: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`

## Troubleshooting

### "DNS check unsuccessful" após 1 hora
- Verifique se os registos A estão corretos
- Certifique-se de que não há registos CNAME conflitantes
- Remova qualquer registo A antigo que aponte para outros IPs

### HTTPS não disponível
- Aguarde até o DNS estar totalmente propagado (pode demorar até 24 horas)
- Certifique-se de que os 4 registos A estão configurados
- Clique em "Check again" no GitHub

### Site não carrega
- Verifique se o ficheiro CNAME no repositório contém `fiderede-lda.com`
- Certifique-se de que o GitHub Pages está ativado
- Aguarde a propagação DNS completa
