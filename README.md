pygame.init()

# Set the screen size
size = (700, 500)
screen = pygame.display.set_mode(size)

# Set the background color to green
green = (0, 255, 0)
screen.fill(green)

# Set the font and text color
font = pygame.font.Font(None, 36)
text = font.render("I love Mimi", True, (255, 255, 255))

# Set the text position
textRect = text.get_rect()
textRect.centerx = screen.get_rect().centerx
textRect.centery = screen.get_rect().centery

# Draw the text
screen.blit(text, textRect)

# Update the screen
pygame.display.flip()

# Wait for the user to close the window
done = False
while not done:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            done = True

# Clean up
pygame.quit()
