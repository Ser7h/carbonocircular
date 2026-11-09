# Carbono Circular | DNS e HTTPS do site

**Registro de conclusão de 09/11/2026.** O GitHub Pages publica o site do repositório `Ser7h/carbonocircular` a partir da raiz da branch `main`. O endereço principal é [https://carbonocircular.com.br/](https://carbonocircular.com.br/).

## Registros DNS em produção

Em 09/11/2026 às 10h22min03s, horário da Bahia (UTC−3), os servidores autoritativos `ns6.wixdns.net` e `ns7.wixdns.net` retornaram os cinco registros abaixo em consultas diretas sem recursão.

| Nome | Tipo | Destino | TTL |
|---|---|---|---|
| `carbonocircular.com.br` | A | `185.199.108.153` | 3.600 s |
| `carbonocircular.com.br` | A | `185.199.109.153` | 3.600 s |
| `carbonocircular.com.br` | A | `185.199.110.153` | 3.600 s |
| `carbonocircular.com.br` | A | `185.199.111.153` | 3.600 s |
| `www.carbonocircular.com.br` | CNAME | `ser7h.github.io` | 3.600 s |

**Histórico da troca.** No painel do Wix, a alteração abrangeu somente os registros A da raiz e o CNAME de `www`. Os três endereços anteriores eram `185.230.63.107`, `185.230.63.171` e `185.230.63.186`. O destino anterior de `www` era `cdn3.wixdns.net`. O Wix confirmou a gravação usando a sessão já autenticada, sem solicitar reCAPTCHA.

## Certificado e HTTPS obrigatório

O GitHub Pages confirmou o estado `approved` para o certificado e `https_enforced: true` para o site. O certificado apresentado pelos servidores passou na validação da cadeia de confiança e do nome do host nas conexões com `carbonocircular.com.br` e `www.carbonocircular.com.br`. Ambos constam no campo de nomes alternativos (SAN). [Configuração do repositório no GitHub Pages](https://github.com/Ser7h/carbonocircular/settings/pages)

A validade do certificado observado vai de **09/11/2026 às 12:21:06 UTC** até **07/02/2027 às 12:21:05 UTC**, conforme os campos `notBefore` e `notAfter`.

## Testes de acesso e redirecionamento

Em 09/11/2026 às 10h22min20s, horário da Bahia (UTC−3), os testes fizeram requisições GET aos quatro endereços e seguiram cada cabeçalho `Location`. Em todos os casos, o conteúdo final foi a página **Carbono Circular · Do resíduo ao solo fértil**.

| Endereço solicitado | Respostas observadas, em ordem |
|---|---|
| `https://carbonocircular.com.br/` | `200 OK` diretamente na raiz |
| `https://www.carbonocircular.com.br/` | `301` para `https://carbonocircular.com.br/`, seguido de `200 OK` |
| `http://carbonocircular.com.br/` | `301` para `https://carbonocircular.com.br/`, seguido de `200 OK` |
| `http://www.carbonocircular.com.br/` | `301` para `http://carbonocircular.com.br/`, depois `301` para `https://carbonocircular.com.br/` e `200 OK` |

A abertura de `https://www.carbonocircular.com.br/` também foi confirmada no Chrome. O navegador exibiu a página no endereço principal `https://carbonocircular.com.br/`.

## Deploy do commit 52e6758

Em 09/11/2026 às **10h39min12s, horário da Bahia (13h39min12s UTC)**, o GitHub Pages registrou a publicação do commit [`52e6758`](https://github.com/Ser7h/carbonocircular/commit/52e6758d287d8c9a7df2910ac62f0934cc78cf4a) da branch `main` no ambiente `github-pages`. As etapas de build e deploy terminaram com sucesso. [Execução 42627175139 no GitHub Actions](https://github.com/Ser7h/carbonocircular/actions/runs/42627175139)

Após o deploy, às **10h40min39s** do mesmo dia, o acesso direto a `https://carbonocircular.com.br/` retornou `200 OK`. Tanto `https://www.carbonocircular.com.br/` quanto `http://carbonocircular.com.br/` retornaram `301 Moved Permanently` e redirecionaram em um único salto para `https://carbonocircular.com.br/`, que respondeu `200 OK`. Os três acessos exibiram a página **Carbono Circular · Do resíduo ao solo fértil**. O certificado passou na validação TLS para a raiz e para `www`, e o Pages manteve o HTTPS obrigatório (`https_enforced: true`).

## Deploy do commit 62f27cc

Em 09/11/2026 às **10h41min59s, horário da Bahia (13h41min59s UTC)**, o GitHub Pages concluiu com sucesso o deploy do commit [`62f27cc`](https://github.com/Ser7h/carbonocircular/commit/62f27cceb86b70351928b0ce787e4f39b5f164c5) da branch `main` no ambiente `github-pages`. [Execução 42627669685 no GitHub Actions](https://github.com/Ser7h/carbonocircular/actions/runs/42627669685)

Às **10h42min33s**, horário da Bahia, `https://carbonocircular.com.br/` respondeu diretamente com `200 OK`. O acesso a `https://www.carbonocircular.com.br/` retornou `301 Moved Permanently` com destino a `https://carbonocircular.com.br/`. Após esse único redirecionamento, a raiz respondeu `200 OK` e exibiu **Carbono Circular · Do resíduo ao solo fértil**. A validação TLS passou nos dois endereços e o GitHub Pages confirmou o HTTPS obrigatório (`https_enforced: true`).

## Deploy do commit fb76c49

Em 09/11/2026 às **10h45min44s, horário da Bahia (13h45min44s UTC)**, o GitHub Pages concluiu com sucesso a publicação do commit [`fb76c49`](https://github.com/Ser7h/carbonocircular/commit/fb76c49e83f5b8ba6d32ce8ba59145c9b4f5ec29) da branch `main` no ambiente `github-pages`. [Execução 42628162197 no GitHub Actions](https://github.com/Ser7h/carbonocircular/actions/runs/42628162197)

Às **10h46min02s**, horário da Bahia, `https://carbonocircular.com.br/` respondeu diretamente com `200 OK` e exibiu **Carbono Circular · Do resíduo ao solo fértil**. O acesso a `https://www.carbonocircular.com.br/` retornou `301 Moved Permanently` para `https://carbonocircular.com.br/`. A raiz respondeu `200 OK` após esse único redirecionamento. O certificado passou na validação TLS para os dois nomes e o GitHub Pages confirmou o HTTPS obrigatório (`https_enforced: true`).

## Deploy do commit 197128f

Em 09/11/2026 às **10h48min36s, horário da Bahia (13h48min36s UTC)**, o GitHub Pages concluiu com sucesso a publicação do commit [`197128f`](https://github.com/Ser7h/carbonocircular/commit/197128ff5f3f0bb6d1f5f165f9828ba1b191edb1) da branch `main` no ambiente `github-pages`. [Execução 42628615704 no GitHub Actions](https://github.com/Ser7h/carbonocircular/actions/runs/42628615704)

Às **10h50min52s**, horário da Bahia, `https://carbonocircular.com.br/` respondeu diretamente com `200 OK`. O acesso a `https://www.carbonocircular.com.br/` retornou `301 Moved Permanently` com destino a `https://carbonocircular.com.br/`. Após esse único redirecionamento, a raiz respondeu `200 OK` e exibiu **Carbono Circular · Do resíduo ao solo fértil**. A validação TLS passou nos dois endereços, e o GitHub Pages confirmou o HTTPS obrigatório (`https_enforced: true`).

## Deploy do commit 19dec9d

Em 09/11/2026 às **10h57min17s, horário da Bahia (13h57min17s UTC)**, o GitHub Pages concluiu com sucesso a publicação do commit [`19dec9d`](https://github.com/Ser7h/carbonocircular/commit/19dec9d8165d3c0d28d8153917f7d13bc5532c13) da branch `main` no ambiente `github-pages`. [Execução 42629821057 no GitHub Actions](https://github.com/Ser7h/carbonocircular/actions/runs/42629821057)

Este é o commit final da migração. A verificação posterior, feita às **11h00min07s** do mesmo dia, confirmou `https://carbonocircular.com.br/` respondendo `200 OK` com corpo de SHA-256 `7fcaf337a877d035150d41139509ce2680b8501f7a59d12b0d9bc4c5eb6c3605`. O redirecionamento de `www` e de HTTP para a raiz em HTTPS ocorreu em um único salto, e o GitHub Pages manteve o HTTPS obrigatório (`https_enforced: true`).

## Comandos de conferência

No PowerShell, os comandos abaixo consultam os dois servidores DNS e exibem o estado do certificado e do HTTPS obrigatório no GitHub Pages.

```powershell
foreach ($servidor in '216.239.32.100', '216.239.34.100') {
    Resolve-DnsName carbonocircular.com.br -Type A -Server $servidor -DnsOnly -NoRecursion
    Resolve-DnsName www.carbonocircular.com.br -Type CNAME -Server $servidor -DnsOnly -NoRecursion
}
gh api repos/Ser7h/carbonocircular/pages --jq '{cname, https_enforced, https_certificate}'
```

Para reproduzir os quatro testes de acesso, o comando exibe o status e o destino de cada redirecionamento. A validação TLS do `curl` fica habilitada.

```powershell
foreach ($url in 'https://carbonocircular.com.br/', 'https://www.carbonocircular.com.br/', 'http://carbonocircular.com.br/', 'http://www.carbonocircular.com.br/') {
    Write-Output $url
    curl.exe --silent --show-error --location --max-redirs 5 --dump-header - --output NUL $url |
        Select-String '^(HTTP/|Location:)'
}
```
