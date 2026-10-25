# RG2 Rotas — PWA para Motoboy

## Arquivos
- `index.html`: interface e mapa
- `manifest.webmanifest`: configuração instalável
- `sw.js`: cache básico da interface
- `icons/`: ícones do app

## Recursos
- Importa JSON/GeoJSON; pontos viram destinos e linhas são desenhadas no mapa.
- Aceita coordenadas, endereços e alguns links completos do Google Maps.
- GPS atual e distância em linha reta até o próximo destino.
- Cálculo de rota pelas ruas via OSRM, com estimativa de distância/duração e uma instrução inicial resumida.
- Abre o destino no Google Maps para navegação curva a curva e voz.
- Salva rotas localmente no navegador, reabre e exclui rotas, e exporta a rota como GeoJSON.
- PWA: manifesto, instalação quando suportada e cache básico da interface.

## Publicar
Envie todos os arquivos e a pasta `icons` para a raiz do mesmo projeto no GitHub Pages ou Vercel. A hospedagem precisa ser HTTPS para GPS, PWA e service worker.

## Limitações importantes
- Rotas salvas ficam no armazenamento local daquele navegador/aparelho; não sincronizam entre dispositivos.
- Cache offline guarda apenas parte da interface. Mapa, tiles, geocodificação e cálculo de rotas precisam de internet.
- O OSRM público é um serviço de demonstração sem SLA/garantia de uso ilimitado. Para produção, use um provedor de roteamento com condições adequadas.
- A rota usa perfil rodoviário genérico, não especificamente motocicleta. A instrução de manobra no site é resumida; para voz e curva a curva, abra o Google Maps.
- Links curtos do Google Maps podem não expor coordenadas. Cole coordenadas ou link completo quando necessário.
- Não use o celular enquanto pilota.
