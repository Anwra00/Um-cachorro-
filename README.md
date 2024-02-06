import turtle

# Configurar a tartaruga
t = turtle.Turtle()
t.speed(2)
t.pensize(3)

# Função para desenhar um círculo
def desenhar_circulo(cor, raio, x, y):
    t.penup()
    t.color(cor)
    t.goto(x, y)
    t.pendown()
    t.begin_fill()
    t.circle(raio)
    t.end_fill()

# Função para desenhar um retângulo
def desenhar_retangulo(cor, largura, altura, x, y):
    t.penup()
    t.color(cor)
    t.goto(x, y)
    t.pendown()
    t.begin_fill()
    for _ in range(2):
        t.forward(largura)
        t.left(90)
        t.forward(altura)
        t.left(90)
    t.end_fill()

# Desenhar corpo
desenhar_retangulo("brown", 100, 50, -50, -50)

# Desenhar cabeça
desenhar_circulo("brown", 25, 0, 25)

# Desenhar olho esquerdo
desenhar_circulo("black", 5, -10, 40)

# Desenhar olho direito
desenhar_circulo("black", 5, 10, 40)

# Desenhar nariz
t.penup()
t.goto(0, 25)
t.pendown()
t.setheading(-90)
t.forward(10)
t.right(90)
t.forward(15)

# Desenhar orelha esquerda
t.penup()
t.goto(-50, 25)
t.pendown()
t.setheading(90)
t.forward(15)
t.right(90)
t.forward(20)

# Desenhar orelha direita
t.penup()
t.goto(50, 25)
t.pendown()
t.setheading(90)
t.forward(15)
t.left(90)
t.forward(20)

# Manter a janela aberta
turtle.mainloop()
