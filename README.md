# Kafra Market Decrypto Studio

Repositorio de continuidad para **Kafra Market Decrypto Studio**.

Estado actual: **Alpha 1.128 / Engine 1.2.117**.

## Yuno OF4

Alpha 1.128 integra la recuperación **Yuno OF4 -> SPR/ACT canónicos** directamente en Kafra Market y mantiene el criterio conservador del proyecto: un OF4 no se considera recuperado por cambiar su firma ni por extraerse del GRF.

El flujo nuevo puede trabajar 100% offline sobre una carpeta `DECRYPTED_p4y` existente, crea respaldo de cualquier OF4 que sustituya y deja intactos los casos que no pueda demostrar estructuralmente.

Estado privado validado al cerrar esta etapa: **6 recursos críticos reconstruidos** y **32 críticos aún unresolved**. Los binarios recuperados, el corpus OF4 y los diagnósticos siguen fuera de este repositorio público.

## Continuar el trabajo

Lee primero [`docs/HANDOFF_2026-09-11.md`](docs/HANDOFF_2026-09-11.md).

Motor Windows x86 Alpha 1.128 / Engine 1.2.117:

`f75e31b27191cef0d2eb9d9d5243a40a363bd4fde5344c6924fbfaabd9a046d1  Kafra_Decrypto_Universal.exe`

La fuente completa y las entregas privadas se mantienen fuera de GitHub porque contienen conocimiento derivado de assets comprados del usuario. El repositorio público conserva únicamente el handoff técnico y el estado verificable del proyecto.
