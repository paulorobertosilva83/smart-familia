# smart-familia
Aplicativo de controle financeiro familiar
Smart Família — No Positivo

Aplicativo de planejamento financeiro doméstico para acompanhar entradas, saídas, orçamento mensal e fluxo de caixa, identificar quando falta dinheiro e organizar um plano de solução, sem perder de vista a reserva financeira e o lazer em família.



Versão: RC2.1 — candidata para validação.
Situação: desenvolvimento principal implementado e testes locais executados; publicação GitHub Pages e homologação em dispositivos reais ainda precisam ser comprovadas.
Idioma: português brasileiro (pt-BR).

Objetivo

Ajudar a família a tomar decisões práticas para buscar um orçamento positivo: visualizar o que entra e sai, antecipar contas, calcular a necessidade de economia ou renda extra por dia disponível e reservar, quando o orçamento permitir, um valor para momentos de lazer juntos.

O aplicativo não promete renda extra, não realiza investimentos e não substitui aconselhamento financeiro profissional.

Funcionalidades





Visão geral: indicadores do mês, saldo e situação do orçamento.



Entradas e saídas: lançamentos de receitas e despesas realizados ou previstos, com edição e exclusão.



Orçamentos: limites de despesas por categoria e acompanhamento de metas.



Fluxo diário: projeção de saldos por data, recebimentos e contas pendentes, avisos de vencimento e risco de saldo temporariamente negativo.



Plano de solução: simulação de redução de despesas, complementação de receitas e cálculo de quanto falta gerar por dia disponível para atingir a meta.



Reserva e lazer: planejamento de valores destinados à segurança financeira e a atividades em família.



Continuidade mensal: transporte manual e controlado do saldo de um mês encerrado.



Dados: armazenamento local no navegador, exportação CSV e backup/restauração em JSON.



PWA: interface adaptada a celular e computador, com recursos de instalação e cache para acesso offline após carregamento inicial bem-sucedido.

As simulações são cenários hipotéticos; economias e ganhos só devem ser tratados como realizados quando efetivamente ocorrerem.

Como usar





Abra o endereço HTTPS publicado do aplicativo.



Em Configurações, informe saldo inicial, metas de reserva, lazer e demais parâmetros do orçamento.



Em Entradas e saídas, registre receitas e despesas do mês, distinguindo previstas de realizadas.



Consulte Orçamentos e Fluxo diário para acompanhar limites, contas pendentes e possíveis faltas de caixa antes dos vencimentos.



Em Plano de solução, avalie os ajustes de despesas e a meta de complementação de renda por dia.



Faça regularmente um backup JSON e guarde-o em local privado.

Durante a validação, utilize apenas dados fictícios.

Publicação no GitHub Pages

O aplicativo é estático e não exige instalação de Node.js, banco de dados ou etapa de compilação para ser publicado.





Crie um repositório no GitHub, por exemplo, smart-familia.



Envie estes arquivos à raiz do repositório, sem colocá-los em uma subpasta:

 index.html
 manifest.webmanifest
 service-worker.js
 icon-192.png
 icon-512.png
 .nojekyll
 README.md



Acesse Settings → Pages.



Em Build and deployment, escolha Deploy from a branch, selecione main e /(root), depois clique em Save.



Aguarde a disponibilização do link Visit site e verifique o funcionamento no navegador.

Para um repositório chamado smart-familia, na conta paulorobertosilva83, o endereço esperado (não confirmado) é:

https://paulorobertosilva83.github.io/smart-familia/



Atenção: o código hospedado em um repositório público pode ser visto por terceiros. Não envie arquivos de backup .json, planilhas com dados reais, relatórios privados, credenciais ou documentos pessoais.

Instalação e uso offline

Em navegador compatível, acesse primeiro o site por HTTPS. Após o carregamento e a instalação/cache dos arquivos, o aplicativo poderá ser aberto como PWA e ter funcionamento offline para recursos estáticos. Esse comportamento ainda precisa ser testado em dispositivos reais, especialmente após fechar e reabrir o navegador e desligar a conexão.

Privacidade e limitações





Os lançamentos são mantidos no armazenamento local do navegador (localStorage), não em um banco de dados na nuvem.



Netlify e GitHub Pages não sincronizam informações automaticamente; cada origem e dispositivo mantém dados próprios.



O armazenamento local pode ser perdido ao limpar dados do navegador, mudar de aparelho ou usar navegação privada. O backup JSON é importante.



Os dados locais não possuem, nesta versão, criptografia própria ou autenticação de usuários.



Não há integração bancária, sincronização entre familiares ou execução automática de operações financeiras.



A publicação online, por si só, não comprova a segurança ou a homologação financeira do aplicativo.

Estado de validação







Verificação



Situação registrada





Preparação local Windows e integridade dos pacotes



PREPARACAO_LOCAL_PASS





Testes de funções com cenários controlados



PASS_LOCAL





Simulação de service worker



PASS_LOCAL





Testes reais no navegador Windows



NOT_RUN





Publicação GitHub Pages e validação da URL



NOT_RUN





Testes Android U01–U15



0/15 — NOT_RUN





Homologação final e liberação para dados reais



PENDENTE

Atenção: a publicação via Netlify foi informada pelo responsável, mas não foi verificada neste README por URL e evidências de acesso. A RC2.1 permanece candidata / NO-RELEASE.

Próximas etapas

Publicar e conferir a URL HTTPS; validar funcionalidades no Windows; executar os 15 testes Android (priorizando persistência, offline e recuperação de backup); encaminhar falhas reproduzidas ao Codex; repetir regressões e registrar o aceite final.

Licenciamento

Nenhuma licença de código aberto foi definida para este repositório. O arquivo README.md não concede, por si só, permissão de reprodução ou redistribuição do código.
