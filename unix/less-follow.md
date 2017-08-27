# Less Follow

Similar to `tail -f`, `less` can actually follow a file as well as it's default edit mode. 

## Usage

Using `less +F` watches the file and follows it's tail - updating the screen as it grows. 

Using the <kbd>F</kbd> key whist in read mode will enter into less' watch mode. Conversely, pressing <kbd>CTRL</kbd> - <kbd>C</kbd> in watch mode will return you to read mode - enabling the ability to quickly toggle between watch and read/edit modes.