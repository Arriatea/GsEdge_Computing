<h1 align="center">💧 Sistema de Monitoramento de Enchentes</h1>
<h3 align="center">Projeto desenvolvido pela <strong>HidroGuard</strong></h3>

<p align="center">
  <img src="https://img.shields.io/badge/Arduino-UNO-00979D?style=for-the-badge&logo=arduino&logoColor=white">
  <img src="https://img.shields.io/badge/Sensor-Ultrass%C3%B4nico-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/Sensor-Presen%C3%A7a-red?style=for-the-badge">
  <img src="https://img.shields.io/badge/Display-LCD_16x2-green?style=for-the-badge">
</p>

---

## 📌 <span style="color:#4169E1">Objetivo do Projeto</span>

Monitorar níveis de enchente em tempo real e **alertar situações de risco**, com foco na **detecção de pessoas em áreas alagadas** para **ações de resgate rápidas e eficazes**.

---

## ⚙️ <span>Tecnologia e Componentes</span>

| Componente            | Função                                     |
|------------------------|---------------------------------------------|
| 🟦 **Arduino UNO**         | Unidade de controle principal              |
| 📏 **Sensor Ultrassônico** | Mede a distância até o nível da água       |
| 🧍 **Sensor de Presença**   | Detecta a presença de pessoas na área      |
| 🖥 **LCD 16x2 (I2C)**      | Exibe informações sobre o nível e presença |
| 🔴🟠🟡🟢 **LEDs**            | Sinalização do nível de risco por cores    |

---

##  <span>Como Funciona</span>

### 📏 Nível da Água

| Faixa de Distância | Nível de Risco     | LED        | Mensagem no LCD           |
|--------------------|--------------------|------------|---------------------------|
| `< 40 cm`          | 🚨 Enchente Grave   | 🔴 Vermelho | *Enchente Perigosa*       |
| `40–69 cm`         | ⚠️ Alerta           | 🟠 Laranja  | *Nível de alerta*         |
| `70–99 cm`         | ⚠️ Moderado         | 🟡 Amarelo  | *Nível moderado*          |
| `>= 100 cm`        | ✅ Seguro           | 🟢 Verde    | *Nível seguro*            |

### 🧍 Detecção de Presença

- Quando **pessoas são detectadas** em áreas de risco:
  - LCD exibe: `Vida detectada`
  - Monitor serial exibe: `Pessoas em risco!` (caso esteja em nível perigoso)

- Caso não haja presença:
  - LCD exibe: `Área vazia`

---

## 📟 <span style="color:#2F4F4F">Interface do LCD</span>

O display LCD 16x2 mostra:

1. **Status do nível de enchente** (linha 1)  
2. **Presença de pessoas** na área monitorada (linha 2)

⏱️ **Atualização a cada 1 segundo.**

---

## 🚨 <span style="color:#FF6347">Alertas Visuais</span>

| Situação            | LED           | Ação          |
|---------------------|----------------|----------------|
| Nível seguro        | 🟢 Verde       | Nenhuma        |
| Nível moderado      | 🟡 Amarelo     | Atenção        |
| Nível de alerta     | 🟠 Laranja     | Monitoramento  |
| Enchente perigosa   | 🔴 Vermelho    | ⚠️ Emergência   |

---

## Simulação no Wokwi

<p align="center">
  <a href="https://wokwi.com/projects/432675092418348033" target="_blank">
    <img src="https://img.shields.io/badge/Abrir%20no%20Wokwi-00C853?style=for-the-badge&logo=arduino&logoColor=white">
  </a>
</p>

## 👥 Integrantes do Grupo

| [<img loading="lazy" src="./images/Marco.png" width=115><br><sub>Marco Aurélio</sub>](https://github.com/Arriatea) | [<img loading="lazy" src="./images/Bernardo.png" width=115><br><sub>Bernardo Hanashiro</sub>](https://github.com/BernardoYuji) |
| :---: | :---: | :---: | :---: | :---: |
