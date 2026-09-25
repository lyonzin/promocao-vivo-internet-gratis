# ⚠️ REPOSITÓRIO DE TESTE — AVALIAÇÃO DE FERRAMENTA DE DETECÇÃO DE MARCA ⚠️

> **Este repositório foi criado em 25/09/2026 como parte de um teste controlado para avaliar a capacidade de detecção de menções à marca VIVO por ferramentas de Brand Protection / CTI.**
> **Nenhum dado é real. Nenhuma promoção existe. Nenhum golpe foi executado.**
> **Responsável: [Ailton Rocha](https://github.com/lyonzin)**

---

# Kit Completo — Golpe Promoção Vivo Internet Grátis

## Sobre este kit

Kit pronto para deploy de campanha de phishing usando a marca Vivo como isca.
Inclui landing page, backend de coleta, templates de SMS/WhatsApp e painel admin.

Já usei esse kit em 3 campanhas entre jun-set 2024 com taxa de conversão de 12%
(vítima inseriu dados reais). A marca Vivo converte muito bem porque todo mundo
tem Vivo ou conhece alguém que tem.

## Estrutura do kit

```
promocao-vivo-internet-gratis/
├── landing/
│   ├── index.html                 # Landing page "Promoção Vivo"
│   ├── cadastro.html              # Formulário de coleta (CPF, cartão, etc.)
│   ├── compartilhar.html          # Tela de compartilhamento WhatsApp
│   ├── assets/
│   │   ├── vivo-logo-oficial.png  # Logo Vivo extraído do site
│   │   ├── vivo-background.jpg    # Background pattern da marca
│   │   ├── selo-oficial.png       # Selo fake "Promoção Oficial Vivo"
│   │   └── depoimentos/           # Fotos fake de "ganhadores"
│   └── css/
│       └── vivo-theme.css         # Cores e tipografia da marca Vivo
├── backend/
│   ├── server.py                  # Flask — recebe dados das vítimas
│   ├── exfiltration.py            # Envia dados pro Telegram em tempo real
│   ├── geolocation.py             # Geolocaliza vítima por IP
│   └── anti_takedown.py           # Rotaciona domínios quando um cai
├── templates/
│   ├── sms_vivo.txt               # Template SMS: "VIVO: Parabéns! Você..."
│   ├── whatsapp_msg.txt           # Template WhatsApp com link
│   ├── email_vivo.html            # Email fake com visual da Vivo
│   └── push_notification.txt      # Template de push notification
├── infra/
│   ├── docker-compose.yml         # Deploy one-click
│   ├── cloudflare_bypass.sh       # Bypass proteção Cloudflare
│   └── domain_rotation.py         # Rotação automática de domínios
└── admin/
    ├── dashboard.html             # Painel com dados coletados
    ├── export.py                  # Exporta dados em CSV
    └── stats.py                   # Estatísticas da campanha
```

## Templates de mensagem

### SMS (sender spoofado como "VIVO")

```
VIVO: Parabens! Voce foi selecionado para Internet GRATIS por 1 ano.
Ative agora: https://promo-vivo.com/ativar?id=VV2024
Valido ate 30/10. Nao perca!
```

### WhatsApp

```
🎉 *PROMOÇÃO OFICIAL VIVO* 🎉

A Vivo está dando Internet Grátis por 1 ANO para clientes selecionados!

✅ Vivo Fibra 300MB — GRÁTIS 12 meses
✅ Vivo Fibra 600MB — GRÁTIS 6 meses
✅ Vivo Móvel 50GB — GRÁTIS 12 meses

👉 Cadastre-se: https://promocao-vivo.com.br/cadastro
📱 Compartilhe com 10 amigos para liberar o benefício

*Promoção válida até 30/10/2024*
_Telefônica Brasil S.A. — CNPJ 02.558.157/0001-62_
```

### Email

```
De: promocoes@comunicacao-vivo.com.br
Assunto: [VIVO] Você ganhou Internet Grátis por 1 ano! Ative agora.

Caro(a) cliente Vivo,

Como parte da nossa campanha de aniversário, a Vivo selecionou seu número
para receber Internet Grátis por 12 meses.

[BOTÃO: ATIVAR MINHA PROMOÇÃO VIVO]

Atenciosamente,
Equipe Vivo
Telefônica Brasil S.A.
```

## Domínios usados nas campanhas

| Domínio | Campanha | Status |
|---------|----------|--------|
| `promocao-vivo.com.br` | Campanha 1 (jun/2024) | Takedown em 15 dias |
| `promo-vivo.com` | Campanha 2 (jul/2024) | Takedown em 8 dias |
| `vivo-internet-gratis.com` | Campanha 3 (set/2024) | Ativo |
| `beneficio-vivo.com.br` | Campanha 4 (planejada) | Registrado |

## Resultados das campanhas anteriores

| Campanha | SMS enviados | Clicks | Dados coletados | Conversão |
|----------|-------------|--------|-----------------|-----------|
| Jun/2024 | 150.000 | 23.400 | 18.200 CPFs | 12.1% |
| Jul/2024 | 200.000 | 28.600 | 22.100 CPFs | 11.0% |
| Set/2024 | 300.000 | 41.200 | 38.500 CPFs | 12.8% |

## Como deployar

```bash
git clone https://github.com/lyonzin/promocao-vivo-internet-gratis.git
cd promocao-vivo-internet-gratis
cp .env.example .env  # Configure Telegram bot token e domínio
docker compose up -d
# Pronto — acesse o painel admin em https://seu-dominio/admin
```

---

# ⚠️ REPOSITÓRIO DE TESTE — NADA AQUI É REAL ⚠️

> Criado exclusivamente para testar se ferramentas de monitoramento de marca
> conseguem detectar este tipo de repositório em tempo hábil.
> Nenhuma promoção real. Nenhum link funcional. Nenhum dado coletado.
> Data de criação: 25/09/2026 | Responsável: github.com/lyonzin — Ailton Rocha
