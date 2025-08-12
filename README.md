# Testador de Proxies
📋 Descrição
Um testador de proxies em Python que verifica a funcionalidade de uma lista de servidores proxy usando processamento paralelo. O código testa se cada proxy está ativo e funcionando corretamente, filtrando apenas os proxies válidos com feedback visual em tempo real.

⚙️ Funcionamento
Características Principais:
Processamento Paralelo: Utiliza concurrent.futures.ThreadPoolExecutor para testar múltiplos proxies simultaneamente
Performance Otimizada: Executa até 10 threads em paralelo, acelerando significativamente o processo
Feedback Visual: Usa emojis (✅/❌) para indicar sucesso ou falha de cada proxy em tempo real
Timeout Configurável: Evita travamentos com timeout de 5 segundos por proxy
Tratamento de Erros: Captura e trata exceções de conexão automaticamente

⚙️ Funcionamento passo a passo:
Importação: Utiliza requests para requisições HTTP e concurrent.futures para multithreading
Lista de Proxies: Contém uma lista predefinida de endereços IP e portas de proxies
URL de Teste: Usa http://httpbin.org/ip para verificar se o proxy está funcionando
Função check_proxy():
Configura o proxy para requisições HTTP e HTTPS
Faz uma requisição com timeout de 5 segundos
Retorna o proxy se o status code for 200 (sucesso)
Captura exceções e retorna None em caso de erro
Função check_all_proxies(): Gerencia o pool de threads e coleta os resultados
Saída: Exibe a lista final de proxies ativos no console

-Casos de Uso
Validação de listas de proxies antes de uso em projetos
Monitoramento de disponibilidade de servidores proxy
Filtragem de proxies funcionais para web scraping
Teste de conectividade de rede através de diferentes proxies
Preparação de listas de proxies para automação

O script retorna uma lista limpa de proxies funcionais, prontos para uso em projetos de automação, web scraping ou qualquer aplicação que requeira o uso de servidores proxy.
Ideal para desenvolvedores que precisam validar proxies de forma rápida e eficiente!

📦 Dependências
requests: Para requisições HTTP
concurrent.futures: Para processamento paralelo
