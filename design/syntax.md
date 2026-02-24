# Syntax Draft

LambdaTesseract programs are defined as flows of transformations.

Example:

flow main:
    read@stdin
    |> hash@sha256
    |> verify@policy
    |> write@stdout
end
