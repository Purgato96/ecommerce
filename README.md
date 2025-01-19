# E-commerce Platform

Este projeto é uma plataforma de e-commerce desenvolvida com a **stack LIVT** (Laravel, Inertia.js, Vue.js, TailwindCSS), utilizando Docker com Laravel Sail para configuração do ambiente. A aplicação é modular, flexível e escalável, permitindo que lojistas criem lojas virtuais de forma personalizada, com opções adicionais, como integração com blog e ferramentas externas.

## **Funcionalidades Planejadas**
- Cadastro e autenticação de usuários (lojistas, gestores, etc.).
- Controle de Acesso (ACL) com permissões específicas:
    - Setor de produtos.
    - Setor de blog.
    - Setor financeiro.
    - Setor de entregas.
    - Integração com marketplaces (via Bling).
- Integração com a API do **Bling** para sincronização de dados.
- Blog integrado para otimização de SEO e marketing de conteúdo.
- Rotas e interfaces rápidas, responsivas e otimizadas para SEO.

## **Planos de Serviço**
1. **Plano Básico**:
    - Loja virtual completa.
2. **Plano Premium**:
    - Loja virtual com blog integrado.
    - Recursos adicionais de SEO.

## **Tecnologias Utilizadas**
- **Laravel**: Framework backend robusto e escalável.
- **Inertia.js**: Comunicação entre o backend e o frontend sem APIs REST ou GraphQL.
- **Vue.js**: Framework progressivo para o frontend.
- **TailwindCSS**: Framework de CSS para estilização moderna e responsiva.
- **Docker com Sail**: Ambiente de desenvolvimento containerizado.
- **MySQL**: Banco de dados relacional.
- **Bling**: Integração com sistema de gestão empresarial.

## **Instalação**
### Pré-requisitos
- Docker Desktop configurado no sistema.
- Composer instalado localmente (opcional, para usuários que não utilizam Docker).
- Node.js e npm instalados (para desenvolvimento frontend).

### Passos
1. Clone este repositório:
   ```bash
   git clone https://github.com/Purgato96/ecommerce.git
   cd ecommerce

2. Instale as dependências do backend e do frontend:
   ```bash 
   ./vendor/bin/sail composer install
   ./vendor/bin/sail npm install

3. Gere o arquivo .env e configure-o:
    ```bash
    cp .env.example .env
    ./vendor/bin/sail artisan key:generate

4. Suba os containers Docker:
    ```bash 
    ./vendor/bin/sail up -d

5. Execute as migrações e seeders:
    ```bash 
    ./vendor/bin/sail artisan migrate --seed

6. Acesse a aplicação no navegador: http://localhost.

##  Estrutura do Projeto
- /app: Contém os controladores, modelos e serviços do backend.
- /resources: Contém as views e componentes Vue.js do frontend.
- /database: Migrações, seeders e factories.
- /routes: Arquivos de rotas do Laravel.
- /public: Arquivos estáticos como imagens e CSS.

## Contribuindo
Sinta-se à vontade para abrir issues ou pull requests neste repositório para sugerir melhorias ou reportar bugs.

1. **Faça um fork do projeto.**
2. **Crie uma branch para suas alterações:** 
    ```bash
    git checkout -b minha-nova-feature

3. Faça o commit das alterações:
   ```bash
   git commit -m "Descrição da minha nova feature"

4. Faça o push para a branch:
   ```bash
    git push origin minha-nova-feature

5. Abra um pull request.

## Licença
Este projeto está licenciado sob a MIT License.
