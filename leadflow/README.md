# LeadFlow Instagram

CRM leve para captação e gestão de contatos, com Supabase Auth + Postgres e publicação estática no Cloudflare Pages.

## Funcionalidades
- Login e cadastro por e-mail/senha.
- Primeiro usuário configura o espaço e recebe papel de administrador.
- Convites individuais para funcionários (token de uso único, expira em 7 dias).
- Leads compartilhados na equipe, etapas de funil, notas, importação e exportação CSV.
- Módulo de prospecção pública: pesquisa por segmento/cidade na web e Google Maps, cadastro de empresas com telefone comercial publicado, registro da URL de origem e classificação entre empresa e pessoa física.
- Registro da base de contato (`public_business_contact`, `consent`, `inbound` ou `existing_relationship`) para apoiar a governança da lista.
- Formulário público de cadastro e formulário para link da bio do Instagram.
- Consentimento de contato registrado no momento da captação.
- Row Level Security nas tabelas expostas.

## Configuração
O app usa a chave publishable do Supabase no navegador. Chaves service_role/secret nunca devem ser publicadas.
Projeto Supabase: https://appgmuqpqyzkfflzhuws.supabase.co
Região: sa-east-1 (São Paulo).

## Prospecção responsável
A pesquisa abre resultados públicos no navegador; não coleta automaticamente dados do Instagram, não extrai telefones privados de seguidores e não contorna limites da plataforma. Cadastre empresas somente com canais divulgados pela própria empresa para atendimento comercial. Cadastre pessoas físicas somente quando houver solicitação de retorno ou autorização. Guarde a URL da fonte e respeite pedidos de interrupção de contato.

## Publicação
Cloudflare Pages: framework None, build command vazio, build output directory `leadflow` (se o root directory for a raiz do repositório) ou root directory `/leadflow` e output directory `.`.


Deployment trigger: initial Pages project connected to this branch.
