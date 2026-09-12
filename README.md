# Kafra Market Decrypto Studio

Repositorio de continuidad para **Kafra Market Decrypto Studio**.

Estado actual: **Alpha 1.129 / Engine 1.2.118**.

## Yuno OF4

Alpha 1.129 mantiene la recuperación **Yuno OF4 -> SPR/ACT canónicos** integrada en Kafra Market y corrige el fallo real de Alpha 1.128 durante el post-proceso sobre `DECRYPTED_p4y`.

El diagnóstico de Alpha 1.128 mostró que el engine Windows x86 llegaba a ~2.0 GB y abortaba con `fatal error: out of memory`. La causa era retener cuerpos OF4 completos y candidatos globales de bloques durante el escaneo.

Alpha 1.129 cambia el flujo a memoria acotada:

- descubrimiento OF4 por streaming;
- cada target conserva únicamente metadata, hashes y su prefijo protegido;
- indexación de SPR/ACT estándar limitada a tamaños que realmente pueden ayudar a targets OF4;
- mapas exact/body limitados a hashes solicitados por targets reales;
- candidatos de bloques de 16 bytes construidos bajo demanda;
- backup de originales por streaming;
- límite defensivo del heap Go de 1200 MiB durante el post-proceso OF4;
- progreso visible cada 25,000 SPR/ACT.

El criterio conservador no cambia: un OF4 no se sustituye si la reconstrucción no pasa validación estructural. Los casos no demostrables permanecen `unresolved` e intactos.

Estado privado validado: **6 recursos críticos reconstruidos** y **32 críticos aún unresolved**. Los binarios recuperados, el corpus OF4 y los diagnósticos siguen fuera de este repositorio público.

## Snapshot Alpha 1.129

Engine Windows x86 1.2.118:

`89fc341854cd0eb1b510fefbac7eded71246b48502894dbc1a1cce71fe9c4b09  Kafra_Decrypto_Universal.exe`

Hotfix OF4 listo:

`e5249db2ea19e13a4bff45ea4a86ed326c2d7e94009cc9ab6ba3e2b1e5264443  Kafra_Yuno_OF4_HOTFIX_1.129_READY.zip`

Fuente privada buildable:

`311a0c17613da9643e3183d0c8bd137a4f9e94e7f7454cf1a8ca144c58cb89b7  Kafra_Market_Decrypto_Studio_v2.0.0-alpha.1.129_OFFLINE_OF4_LOW_MEMORY_SOURCE_BUILDABLE.zip`

## Continuar el trabajo

Lee primero [`docs/HANDOFF_2026-09-11.md`](docs/HANDOFF_2026-09-11.md).

La fuente completa y las entregas privadas se mantienen fuera de GitHub porque contienen conocimiento derivado de assets comprados del usuario. El repositorio público conserva únicamente el handoff técnico y el estado verificable del proyecto.
