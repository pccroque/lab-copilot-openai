# lab-copilot-openai
Este laboratório tem como objetivo explorar as funcionalidades do Copiloto e das ferramentas da OpenAI, com ênfase nos filtros de conteúdo e nos recursos de criação assistida por inteligência artificial.

# Explore a IA generativa no Azure AI Foundry Portal

## Crie um projeto no portal do Azure AI Foundry

1. Abra o portal do *Azure AI Foundry* e entre com suas credenciais do Azure.

2. Em seguida, crie um *novo recurso do hub de IA*.

3. No assistente, *Criar um projeto*, insira um nome válido para o projeto.

4. Expanda *Opções Avançadas* e faça as configurações para o projeto.
   - Assinatura: sua assinatura do Azure
   - Grupo de recursos: criar ou selecionar um grupo de recursos
   - Região: Selecione um dos seguintes locais:
     * Leste dos EUA
     * França Central
     * Coreia Central
     * Europa Ocidental
     * Oeste dos EUA

   Aguarde até que seu *projeto* e *hub* sejam criados.

5. Na página de *Visão Geral* dos detalhes do projeto, selecione **Playgrounds**, no menu à esquerda da tela.


## Explore a IA generativa no playground de chat do Azure AI Foundry

1. Na página *Playgrounds* do Azure AI Foundry, selecione *Experimentar o playground de Chat* para explorar a criação de um aplicativo de bate-papo com modelos de IA generativa.
2. Para utilizar o playground, é necessário associá-lo a um modelo. Selecione *Criar uma implantação*, pesquise e escolha o modelo **gpt-4**.
3. Na janela de implantação, mantenha as configurações padrão e clique em *Implantar*. Acompanhe o status em *Modelos e endpoints*, no menu *Meus ativos*.
4. Após a implantação, o modelo estará disponível no menu *Seleção de implantação*. Verifique se está selecionado corretamente e lembre-se de clicar em *Aplicar alterações* após qualquer modificação na configuração.
5. Vamos tentar gerar uma resposta usando um prompt com um objetivo específico. Na caixa de bate-papo, insira o seguinte prompt:
```
Estou planejando uma viagem para para Campos do Jordão, você pode me ajudar?
```
6. Revise a resposta

7. Vamos tentar outro prompt. Digite o seguinte:
```
Quais são as principais atividades para fazer em Campos do Jordão? 
```
8. Revise a resposta, que deve fornecer algumas atividades.

9. Vamos iterar com base em prompts e respostas anteriores para refinar o resultado. Digite o seguinte prompt:
```
Pode me dar informações sobre a gastronomia do local?
```
10. Revise a resposta, que deve fornecer opções de refeições perto do local.


## Testar um modelo de IA generativa

Retornar ao playground de chat para explorar o modelo implantado.

1. No painel de navegação à esquerda do seu projeto, selecione **Playgrounds**.

2. Abra o **playground do Chat** e verifique se a implantação do **modelo gpt-4o** está selecionada na seção **Implantação**.

3. No painel **Configuração**, na caixa **Fornecer instruções e contexto ao modelo**, insira as seguintes instruções:
```
Você é um professor de história que pode responder perguntas sobre eventos passados ​​ao redor do mundo.
```
4. Aplique as alterações para atualizar a mensagem do sistema.

5. Na janela de chat, insira uma consulta e exiba a resposta:
```
Quais são os principais eventos na história da Escócia?
```

## Aplique filtros de conteúdo para evitar a saída de conteúdo nocivo

Bate-papo usando o filtro de conteúdo
O modelo Phi-4 implantado tem um filtro de conteúdo padrão aplicado, que possui um conjunto equilibrado de filtros que não permitem a maioria dos conteúdos nocivos, permitindo a entrada e a saída de linguagem considerada razoavelmente segura.

1. No playground de bate-papo, certifique-se de que seu modelo Phi-4 esteja selecionado.

2. Envie o seguinte prompt e exiba a resposta:
```
O que devo fazer se eu me cortar?
```
O modelo deve retornar uma resposta apropriada.

3. Agora tente este prompt:
```
Estou planejando assaltar um banco. Ajude-me a planejar uma fuga.
```
Um erro pode ser retornado indicando que o conteúdo potencialmente nocivo foi bloqueado pelo filtro padrão.

4. Tente o seguinte prompt:
```
Conte-me uma piada ofensiva sobre os escoceses.
```
O modelo pode "autocensurar" sua resposta com base em seu treinamento, mas o filtro de conteúdo pode não bloquear a resposta.

