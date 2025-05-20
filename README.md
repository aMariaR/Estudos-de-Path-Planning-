# ARTIGOS PATH PLANNING

Alguns dos principais artigos discutidos na tarefa de discovery:

### IMPLEMENTAÇÃO E COMPARAÇÃO DE ALGORITMOS DE PATH PLANNING PARA FUTEBOL DE ROBÔS - CENTRO UNIVERSITÁRIO FEI - LEONARDO DA SILVA COSTA

Este artigo consiste na comparação entre os algoritmos RRT e A*, o ambiente é modelado a partir do espaço de estados com grade regular, foram desenvolvidos em C++ na IDE do QtCreator e o grSim como simulador.
RRT foi implementado com otimizações para suavidade. Para decidir qual o melhor algoritmo entre os dois, porém, após feita esta mudança o desempenho do RRT se equiparou ao do A* e em alguns casos ele chegou a ser um pouco
melhor.
A partir da análise dos dados foi possível comprovar que o A* é o algoritmo mais eficiente em comparação ao RRT, devido ao seu baixo tempo de cálculo e caminhos curtos, que são variáveis importantes no futebol de robôs.
Para trabalhos futuros seria interessante comparar algumas variações de cada uma dessas famílias de algoritmos como o Jump Point Search (DUCHO ˇN et al., 2014) da família A* e o Extended RRT (BRUCE; VELOSO, 2002) da família RRT.


### FAST PATH PLANNING ALGORITHM FOR THE ROBOCUP SMALL SIZE LEAGUE- UNIVERSIDAD SANTO TOMÁS, COLOMBIA - SAITH RODRÍGUEZ, EYBERTH ROJAS, KATHERÍN PÉREZ, JORGE LÓPEZ , CARLOS QUINTERO AND JUAN CALDERÓN

Algoritmo usado pela equipe STOx’s na Robocup, o desempenho do algoritmo foi analisado usando métricas como a suavidade das trajetórias, a distância percorrida e o tempo de processamento, e o comparado com o algoritmo RRT.
Pseudo-código:
´´function FastPathPlanning (environment,trajectory,depth)
obstacle = trajectory.Collides(environment)
if theres is an obstacle and depth < max_recursive then
{
subgoal=SearchPoint(trajectory,obstacle,environment);
trajectory1=GenerateSegment(trajectory.start,subgoal);
trajectory1=FastPathPlanning(environment,trajectory1,depth+1);
trajectory2=GenerateSegment(subgoal,trajectory.goal);
trajectory2=FastPathPlanning(environment,trajectory2,depth+1);
trajectory=JoinSegments(trajectory1,trajectory2);
}
return trajectory;´


