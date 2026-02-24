# Execution Model

Programs execute as immutable flows of cells.

Each cell performs a transformation and passes output forward.

Execution order:

Input → Transform → Verify → Output → Seal
