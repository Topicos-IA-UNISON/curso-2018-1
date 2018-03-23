---
layout: post
title: "Compromisos para después de Semana Santa"
excerpt_separator: "<!--more-->"
categories:
  - Aprendizaje por refuerzo
tags:
  - golang
  - compromisos
---

Una disculpa por no haber estado posteando lo que se hacía cada semana, 
durante ya casi dos meses, trataré de mantener este *blog* como una bitácora de lo que se ha hecho y lo que se va a hacer
durante el curso.

Como se planteo el martes 20 de marzo, acordamos los siguientes compromisos para después de Semana Santa:

<!--more-->

**Primer avance verificable del juego de Tetris y agente que aprenda a jugar**

*Fecha de revisión: lunes 9 de abril de 2018*

Compromisos a revisar:
  1. Juego de Tetris programado en Go funcionando (con inerface hombre máquina).
  2. Motor de juego representado en forma de modelo de simulación MDP con el fin de ser 
     utilizado por un agente inteligentes (tanto para jugar como para el aprendizaje).
  3. Un primer método de aprendizaje por refuerzo programado y enlazado con el motor de juego de tetris desarrollado.
     En este caso, no es importante que ya funcione el aprendizaje, si no que ya se encuentre programado, con la interface
     necesaria. Las opciones que hemos revisado (es posible implementar otra) son:
     
       - *RL Vainilla*. Esto es, implementar todas las funciones de RL (o un método no muy complicado) con *coarse coding* 
          directamente en *Go* y realizar la simulación. Es mas complicado hacer un agente que funcione de forma muy impresionante 
          pero es seguro la mejor forma de dominar tanto RL como *Go*.
        
       - Utilizar [anyRL](https://github.com/unixpickle/anyrl). Es una librería reaizada por *al menos* un programador de 
          [OpenAi](https://openai.com) y hace uso de redes neuronales. El problema es poner el modelo desarrollado en el formato de 
          [AI Gym](https://gym.openai.com).
        
       - Utilizar la [API para Go de Tensorflow](https://godoc.org/github.com/tensorflow/tensorflow/tensorflow/go). 
          Sin embargo la API es bastante limitada resecto a la que existe para otros lenguajes, como Python.
        
       - Compilar el modelo como biblioteca y usarlo dentro de Python en combinación con Tensorflow. Es la opción más arcana que vimos, 
          pero podría dar buenos resultados.
        
**Ejercicios del [libro de Sutton y Barto](http://incompleteideas.net/book/bookdraft2017nov5.pdf)**

*Fecha de revsión: Lunes 16 de abril de 2018*

Ejerccios a realizar:

  1. Ejemplo 4.2 (Jack's Car Rental, página 63) y el ejercicio 4.5 (sobre el mismo problema, página 64) 
     utilizando el método de programación dinámica de iteración de política.
     
  2. Ejercicio 4.9 (Gambler's problem, página 67) utilizando el método de programacion dinámica de iteración de valor.
  
  3. Ejemplo 6.5 (Windy Gridworld, página 104) y ejercicios 6.9 y 6.10 (sobre el mismo problema, página 105) para 
     el método de aprendizaje SARSA.
  
  4. Ejemplo 6.6 (Cliff Walking, página 106) sobre el método de aprendizaje Q-Learning.
  
  5. Ejemplo 10.1 (Mountain Car Task, página 198 y 199) sobre el método SARSA con semi-gradiente, y *coarse coding*. 



