
--# Main
    function setup()
    function setup()
    displayMode(FULLSCREEN)
   gr = physics.body(EDGE, vec2(0,10), vec2(1000, 10))
gr.type = STATIC
gr.y = 10

wall = physics.body(EDGE, vec2(0, 10), vec2(10, 800))
wall.type = STATIC
wall.y = 10

w = physics.body(EDGE, vec2(1000, 10), vec2(1000, 900))
w.type = STATIC
w.y = 10

roof = physics.body(EDGE, vec2(0, 10), vec2(1000, 10))
roof.type = STATIC
roof.y = 750

ball = physics.body(CIRCLE, 10)
ball.restitution = 1
ball.friction = 0.5
ball.y = math.random(600, 730)
ball.x = math.random(100, 900)

b = physics.body(CIRCLE, 10)
b.restitution = 1
b.friction = 0.5
b.x = WIDTH/2
b.y = HEIGHT/2

ba = physics.body(CIRCLE, 10)
ba.restitution = 1
ba.friction = 0.5
ba.x = 500
ba.y = 300

bal = physics.body(CIRCLE, 10)
bal.restitution = 1
bal.friction = 0.5
bal.x = math.random(100, 900)
bal.y = math.random(300, 600)
end


function draw()

    background(0, 0, 0, 255)
--Walls
fill(127, 127, 127, 255)
rect(0,0, 1000, gr.y)
rect(0, wall.y, 10, 800)
rect(1000, w.y, 10, 800)
rect(0, roof.y, 1000, 10)

--Balls
fill(255, 255, 255, 255)
ellipse(ball.x, ball.y, 40)
fill(255, 0, 0, 255)
ellipse(b.x, b.y, 40)
fill(0, 255, 150, 255)
ellipse(ba.x, ba.y, 40)
fill(255, 255, 0, 255)
ellipse(bal.x, bal.y, 40)

end

function touched(t)
b.x = t.x
b.y = t.y
if t.tapCount == 3 then
ball.y = 600
    end
end

function collide(c)
sound(SOUND_JUMP, math.random(1,2000))
    end
    displayMode(FULLSCREEN)

   gr = physics.body(EDGE, vec2(0,10), vec2(1000, 10))
gr.type = STATIC
gr.y = 10

wall = physics.body(EDGE, vec2(0, 10), vec2(10, 800))
wall.type = STATIC
wall.y = 10

w = physics.body(EDGE, vec2(1000, 10), vec2(1000, 900))
w.type = STATIC
w.y = 10

roof = physics.body(EDGE, vec2(0, 10), vec2(1000, 10))
roof.type = STATIC
roof.y = 750

ball = physics.body(CIRCLE, 10)
ball.restitution = 1
ball.friction = 0.5
ball.y = math.random(600, 730)
ball.x = math.random(100, 900)

b = physics.body(CIRCLE, 10)
b.restitution = 1
b.friction = 0.5
b.x = WIDTH/2
b.y = HEIGHT/2

ba = physics.body(CIRCLE, 10)
ba.restitution = 1
ba.friction = 0.5
ba.x = 500
ba.y = 300

bal = physics.body(CIRCLE, 10)
bal.restitution = 1
bal.friction = 0.5
bal.x = math.random(100, 900)
bal.y = math.random(300, 600)
end
