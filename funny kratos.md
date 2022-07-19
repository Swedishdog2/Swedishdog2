import pygame
import os

pygame.init()

GREEN = (0, 255, 0)
BLUE = (0, 0, 255)
WIDTH, HEIGHT = (800, 800)
WIN = pygame.display.set_mode((WIDTH, HEIGHT))
RECTANGLE = pygame.Rect(300, 400, 40, 80)
RECTANGLE2 = pygame.Rect(280, 500, 300, 40)
RECTANGLE3 = pygame.Rect(500, 400, 40, 80)
textfont = pygame.font.SysFont("monospace", 50)
RANDOMIMAGE = pygame.image.load(os.path.join('HAHAHAHAHAHAHAHAHA!.EXE', 'ScreenShot-2022-1-29_13-57-2.png'))
RANDOMIMAGE2 = pygame.transform.scale(RANDOMIMAGE, (800, 200))
YELLOW = (255, 255, 0)


def main():
    run = True
    while run:
        for event in pygame.event.get():
            if (event.type == pygame.QUIT):
                run = False
                
    pygame.quit()



WIN.fill(YELLOW)
pygame.draw.rect(WIN, BLUE, RECTANGLE)
pygame.draw.rect(WIN, BLUE, RECTANGLE2)
pygame.draw.rect(WIN, BLUE, RECTANGLE3)
textTBD = textfont.render(" :)", 1, BLUE)
text2 = textfont.render("HAHAHAHAHAHAHAHAHA!", 1, BLUE) 
WIN.blit(textTBD, (90, 100))
WIN.blit(text2, (0, 600))
WIN.blit(RANDOMIMAGE2, (0, 175))
pygame.display.update()


if __name__ == "__main__":
    main()
