import pygame
import sys
import random

# Initialize Pygame
pygame.init()

# Set up display
width, height = 800, 600
screen = pygame.display.set_mode((width, height))
pygame.display.set_caption("Catch the Ball")

# Set up colors
white = (255, 255, 255)
black = (0, 0, 0)
red = (255, 0, 0)

# Set up player
player_size = 50
player_x = width // 2 - player_size // 2
player_y = height - player_size - 10

# Set up ball
ball_size = 30
ball_x = random.randint(0, width - ball_size)
ball_y = 0
ball_speed = 5

# Set up clock
clock = pygame.time.Clock()

# Main game loop
while True:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            sys.exit()

    keys = pygame.key.get_pressed()
    if keys[pygame.K_LEFT] and player_x > 0:
        player_x -= 5
    if keys[
