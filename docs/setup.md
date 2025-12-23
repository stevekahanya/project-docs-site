flowchart TD
  A[Start] --> B[Check_Python_3_installed]
  B --> C[Open_terminal_or_command_prompt]
  C --> D[Run_pip_install_pygame]
  D --> E{Pygame_install_successful}
  E -- Yes --> F[Create_demo_game_py_file]
  E -- No --> G[Update_pip_or_fix_permission_issues]
  G --> D
  F --> H[Paste_provided_demo_game_code]
  H --> I[Save_demo_game_py]
  I --> J[Navigate_to_script_folder_in_terminal]
  J --> K[Run_python_demo_game_py]
  K --> L{Window_opens_with_moving_square}
  L -- Yes --> M[Use_arrow_keys_to_move_square]
  M --> N[Close_window_to_exit]
  N --> O[End]
  L -- No --> P[Check_graphical_environment_and_troubleshoot]
  P --> K
