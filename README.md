
![logo](https://github.com/user-attachments/assets/19632fbf-f46b-45ee-a6a7-e86fcdbe2df0)

Exploradores Urbanos 


Bem-vindo ao Exploradores Urbanos! Este projeto é um site para uma agência de viagens especializada em roteiros urbanos, oferecendo experiências únicas para quem deseja explorar o melhor das cidades ao redor do mundo.


🚀 Sobre o Projeto

O Exploradores Urbanos tem como objetivo conectar viajantes a destinos incríveis, fornecendo informações detalhadas, sugestões de passeios e ferramentas para facilitar a jornada dos aventureiros urbanos.

🔥 Principais Funcionalidades

🌎 Página de destinos com informações e dicas
🗺️ Roteiros personalizados para cada estilo de viajante
💬 Blog com conteúdos sobre cultura, gastronomia e curiosidades
🏨 Integração com serviços de hospedagem e reservas
📌 Seção interativa com avaliações e recomendações


🛠️ Tecnologias Utilizadas
Frontend: HTML, CSS, Bootstrep



Vamos juntos explorar o mundo, uma cidade por vez! ✈️🏙️

_____________________________________________________________________________________
Diagrama Conceitual

![image](https://github.com/user-attachments/assets/865f55ee-7e18-4077-a7c0-25ff90c2630b)


_____________________________________________________________________________________
Diagrama Lógico

![image](https://github.com/user-attachments/assets/f97fe516-38dc-44be-9f58-0db70cb385d8)


_____________________________________________________________________________________
Diagrama Físico
CREATE TABLE Passageiro (
    PassageiroID INT PRIMARY KEY AUTO_INCREMENT,
    Nome VARCHAR(100) NOT NULL,
    Email VARCHAR(100) UNIQUE NOT NULL,
    Telefone VARCHAR(20) NOT NULL
);


CREATE TABLE Reserva (
    ReservaID INT PRIMARY KEY AUTO_INCREMENT,
    Data DATE NOT NULL,
    PassageiroID INT NOT NULL,
    DestinoID INT NOT NULL,
    Passagem_idaID INT NOT NULL,
    Passagem_voltaID INT NOT NULL,
    FOREIGN KEY (ClienteID) REFERENCES Passageiro(PassageiroID) ON DELETE CASCADE,
    FOREIGN KEY (PacoteID) REFERENCES Pacote(DestinoID) ON DELETE CASCADE
);


CREATE TABLE Destino (
    DestinoID INT PRIMARY KEY AUTO_INCREMENT,
    Localizacao VARCHAR(150) NOT NULL,
    Descricao TEXT NOT NULL
);
