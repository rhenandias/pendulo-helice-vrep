# Sistema Pêndulo + Hélice no software VREP

Projeto de simulação de uma planta com sistema Pêndulo + Hélice utilizando o software [VREP](https://www.coppeliarobotics.com/). Foi utilizado um agoritmo de controle PID escrito em Python, que se comunica com o VREP através da [VREP API](https://www.coppeliarobotics.com/helpFiles/en/apiOverview.htm).

## Confira um vídeo da simulação: [Pêndulo + Hélice](https://www.youtube.com/watch?v=qVLulCcdXlM)

<img src="/Media/4.png" width="640"> 

## Executando a simulação

Basta abrir o arquivo de cena do VREP e executar um dos scripts em Python

*  `\Python\control1.py` - Script de controle simples, com apenas um setpoint definido
*  `\Python\control2.py` - Script de controle utilizado para a demonstração com diversos setpoints diferentes em sequência

Cenas disponíveis: 

* `\Vrep\Equilibrio.ttt` - Planta simples, para execução do script de controle e controle com múltiplos setpoints
* `\Vrep\Equilibrio - com ruido.ttt` - Planta com adição de elementos de ruido para simular a capacidade do controle de recuperar a posição de setpoint inicial

## Dependências

*  **VREP** - Para rodar o sistema é preciso ter o VREP instalado, o software é  disponibilizado com licensa educacional para [Windows, Mac e Linux](https://www.coppeliarobotics.com/downloads).
*  **Python 3** - O código para realização do controle da planta foi escrito em [Python 3](https://www.python.org/).
*  **Biblioteca Simple PID** - O código utiliza da biblioteca Simple PID, disponível para donwload e com instruções de instalação em: [Simple PID](https://pypi.org/project/simple-pid/).
*  **Biblioteca Matplotlib** - Para realizar o plot de gráficos, foi utilizada a biblioteca Matplotlib, disponível para donwload e com instruções de instalação em: [Matplotlib](https://matplotlib.org/users/installing.html).

## Configurando a VREP API

Para utilizar a VREP API é preciso configurar localmente alguns arquivos. 

Após instalar o VREP, copie do diretório de instalação do VREP para a pasta /python do projeto, os seguintes arquivos:

Arquivo `vrep.py`:
```
V-REP3\V-REP_PRO_EDU\programming\remoteApiBindings\python\python\vrep.py
```

Arquivo `vrepConst.py`:
```
V-REP3\V-REP_PRO_EDU\programming\remoteApiBindings\python\python\vrepConst.py
```
Arquivo `remoteApi.dll` de acordo com a plataforma utilizada:

```
\V-REP3\V-REP_PRO_EDU\programming\remoteApiBindings\lib\lib
```

**Para mais informações de como ativar a Remote API do VREP, consulte a documentação: [Enabling the remote API](https://www.coppeliarobotics.com/helpFiles/en/remoteApiClientSide.htm)**
