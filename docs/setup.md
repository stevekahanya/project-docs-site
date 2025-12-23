Installing a Simple Demo Game Using Pygame
Pygame is a popular Python library for creating simple 2D games. Below is a straightforward guide to install it and run a basic demo game (a window with a moving square). This assumes you have Python 3 installed on your system (download from python.org if not).
Step 1: Install Pygame

Open your terminal or command prompt.
Run the following command to install Pygame via pip (Python's package manager):textpip install pygame
If you encounter permission issues, try adding --user at the end or use a virtual environment.

Step 2: Create the Demo Game Script

Create a new file named demo_game.py using a text editor (e.g., Notepad, VS Code).
Copy and paste the following code into the file:Pythonimport pygame
import sys

# Initialize Pygame
pygame.init()

# Set up the screen
screen = pygame.display.set_mode((800, 600))
pygame.display.set_caption("Simple Demo Game")

# Colors
BLACK = (0, 0, 0)
WHITE = (255, 255, 255)

# Square properties
square_size = 50
square_x = 375  # Center horizontally
square_y = 275  # Center vertically
square_speed = 5

# Main game loop
running = True
while running:
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False

    # Handle key presses for movement
    keys = pygame.key.get_pressed()
    if keys[pygame.K_LEFT]:
        square_x -= square_speed
    if keys[pygame.K_RIGHT]:
        square_x += square_speed
    if keys[pygame.K_UP]:
        square_y -= square_speed
    if keys[pygame.K_DOWN]:
        square_y += square_speed

    # Fill the screen with black
    screen.fill(BLACK)

    # Draw the square
    pygame.draw.rect(screen, WHITE, (square_x, square_y, square_size, square_size))

    # Update the display
    pygame.display.flip()

# Quit Pygame
pygame.quit()
sys.exit()
Save the file.

Step 3: Run the Demo

In your terminal, navigate to the folder containing demo_game.py.
Run the script:textpython demo_game.py
A window should open with a white square on a black background. Use arrow keys to move it around. Close the window to exit.

Troubleshooting

If Pygame doesn't install: Ensure pip is up-to-date with pip install --upgrade pip.
No display? Make sure your system supports graphical output (e.g., not a headless server).