# Shadow-Harvester-Windows-Compatible-Fork
A Windows compatible fork of the Shadow Harvester Night Scavenger mining client with fixes for Windows OS Error 123 (path/filename syntax errors).

🔧 What's Fixed
This fork addresses Windows OS Error 123 that occurs when creating challenge directories due to invalid path characters. The original miner works perfectly on Linux/macOS but fails on Windows with:
FATAL ERROR: Could not create challenge directory: The filename, directory name, or volume label syntax is incorrect. (os error 123)

Changes Made

Modified src/data_types.rs: Added path sanitization function to handle Windows-invalid characters (< > : " / \ | ? *)
Sanitized directory/file names: Challenge IDs, addresses, and nonces are now properly sanitized before creating directories
Preserved all functionality: Mining modes, donation support, and API integration remain unchanged

📋 Original Project
Original Repository: https://github.com/disassembler/shadowharvester
Original Author: @disassembler
All credit for the core mining implementation goes to the original author. This fork only contains Windows compatibility fixes.
