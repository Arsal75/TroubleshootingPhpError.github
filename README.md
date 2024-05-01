# TroubleshootingPhpError.github
1. **Problem**: "Undefined index" notice
   - **Description**: This error occurs when trying to access an array key that doesn't exist.
   - **Solution**: Check if the array key exists using `isset()` or `array_key_exists()` before accessing it.
   - **Example**: 
     ```php
     $array = array("foo" => "bar");
     if(isset($array["baz"])) {
         echo $array["baz"];
     }
     ```

2. **Problem**: "Call to undefined function" error
   - **Description**: This error occurs when trying to call a function that hasn't been defined.
   - **Solution**: Make sure the function is declared or included in the script.
   - **Example**: 
     ```php
     function myFunction() {
         echo "Hello, world!";
     }
     myFunction(); // Call to defined function
     ```

3. **Problem**: "Parse error: syntax error, unexpected" error
   - **Description**: This error occurs due to a syntax mistake in the code.
   - **Solution**: Review the code for any missing or misplaced syntax elements such as braces, semicolons, or parentheses.
   - **Example**: 
     ```php
     $name = "John"
     echo "Hello, $name!"; // Missing semicolon at the end of the line
     ```

4. **Problem**: "Fatal error: Cannot redeclare" error
   - **Description**: This error occurs when trying to define a function or class that has already been defined.
   - **Solution**: Avoid redeclaring the same function or class. Use `include_once` or `require_once` instead of `include` or `require` to include files.
   - **Example**: 
     ```php
     include_once("functions.php");
     include_once("functions.php"); // Will not produce a redeclaration error
     ```

5. **Problem**: "Allowed memory size exhausted" error
   - **Description**: This error occurs when PHP reaches its memory limit.
   - **Solution**: Increase PHP's memory limit in the php.ini file or optimize the code to use less memory.
   - **Example**: 
     ```php
     ini_set('memory_limit', '256M');
     // Or adjust memory_limit in php.ini
     ```

6. **Problem**: "Fatal error: Class 'ClassName' not found" error
   - **Description**: This error occurs when trying to use a class that hasn't been defined or included.
   - **Solution**: Include the file containing the class definition or ensure the class is autoloaded.
   - **Example**: 
     ```php
     require_once("ClassName.php");
     $obj = new ClassName();
     ```
