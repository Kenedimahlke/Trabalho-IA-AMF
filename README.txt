Trabalho de Inteligência Artificial.

Ideia:
BO.IA
Sabemos da importância da saúde, e, temos ciência de que nem todos possuem condições de contratarem um nutricionista para auxiliarem nos cuidados da alimentação.
Por esse motivo, tivemos a ideia de trazer esse sistema. Um sistema, onde a pessoa apenas coloca os itens que possui em sua geladeira e recebe uma receita com foco na alimentação saudável.
Trazendo pontos como benefícios nutricionais, quantidade de calorias e outros tipo de vitaminas e nutrientes.

Utilizamos o modelo local LLava-Llama3 para ser a nossa IA de geração de receita, pois, era a opção mais viável, tanto em custo, quanto também em praticidade.

Às vezes oferece algumas falhas, mas é bastante eficiente pra um modelo local instalado dentro da própria máquina.

Utilizamos a Open WebUI como interface para fazer a interação com o usuário.

O que facilitava bastante apenas precisando inserir nosso modelo local.

Customizamos principalmente o prompt para ficar de acordo com a geração de receitas.

Intruções para rodar o modelo localmente:
1. Baixe e instale o Docker em https://www.docker.com/
2. Faça o download do Ollama em https://ollama.com/ e instale-o
3. Em um terminal, rode o seguinte código: ollama run llava-llama3
4. Em um terminal, rode o seguinte código para instalação do Open WebUI: 
docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
5. Rode o Docker e Inicie o Container Open WebUI, após acesse o navegador do sistema e vá até localhost:3000
6. Após carregar a interface, procure por espaço de trabalho, depois vá em importar modelos. Selecione o Modelo baixado (BO.IA).
