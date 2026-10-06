# 📸 Projeto React Native com Câmera

Este repositório contém um projeto desenvolvido na disciplina de Programação Mobile, com foco em utilização da câmera do dispositivo e compartilhamento de imagens. A aplicação permite que o usuário acesse a câmera do celular, alterne entre câmera frontal e traseira, capture uma foto e compartilhe a imagem em outros aplicativos de mídia disponíveis no sistema.

## Visão geral

O app foi construído com React Native + Expo e usa o módulo `expo-camera` para controlar a câmera do dispositivo. A interação principal acontece em uma única tela, com os seguintes fluxos:

- Solicitação de permissão de acesso à câmera.
- Visualização da câmera em tempo real.
- Alternância entre câmera traseira e frontal.
- Captura de uma foto com o botão de câmera.
- Exibição da imagem capturada em uma pré-visualização.
- Compartilhamento da foto por meio do módulo `expo-sharing`.

## 🚀 Como executar

Antes de iniciar, certifique-se de ter o ambiente configurado para React Native com Expo:

- Node.js instalado
- Expo CLI ou a dependência `expo` configurada no projeto
- Emulador Android/iOS ou um dispositivo físico com o app instalado

### 1. Instale as dependências

```bash
npm install
```

### 2. Inicie o projeto

```bash
npm start
```

### 3. Execute no emulador ou dispositivo

Depois de iniciar o Metro Bundler, escolha uma destas opções:

```bash
npm run android
```

```bash
npm run ios
```

ou use o QR Code com o aplicativo Expo Go em um dispositivo móvel.

## Componentes e estrutura do projeto

### App principal
O arquivo principal da aplicação está em `App.tsx` e é responsável por:

- controlar o estado da câmera (`CameraType`);
- verificar se o usuário concedeu permissão para usar a câmera;
- acessar a referência da câmera com `useRef`;
- capturar a foto usando `cameraRef.current.takePictureAsync()`;
- armazenar a URI da imagem em estado;
- exibir a imagem capturada e disponibilizar a opção de compartilhamento.

### Bibliotecas utilizadas

- `expo-camera`: acesso e controle da câmera do dispositivo.
- `expo-sharing`: envio da foto para outros aplicativos de compartilhamento.
- `@expo/vector-icons`: ícones do botão de alternar câmera, tirar foto e compartilhar.
- `react-native`: construção da interface.

### Fluxo de funcionamento

1. A aplicação verifica se existe permissão para uso da câmera.
2. Se não houver permissão, exibe uma mensagem e um botão para solicitar acesso.
3. Quando a permissão é concedida, a câmera é renderizada na tela.
4. O usuário pode trocar entre a câmera traseira e frontal.
5. Ao pressionar o botão de captura, a foto é salva em memória e sua URI é armazenada.
6. A imagem capturada aparece em uma visualização abaixo da câmera.
7. O botão de compartilhamento envia a foto para outros aplicativos compatíveis.

## Estrutura de arquivos

```bash
projeto-react-native-usando-camera/
├── App.tsx
├── app.json
├── assets/
├── index.ts
├── package.json
├── package-lock.json
├── tsconfig.json
├── README.md
```

## Funcionalidades implementadas

- Permissão de acesso à câmera
- Alternância entre câmera frontal e traseira
- Captura de foto em tempo real
- Pré-visualização da imagem capturada
- Compartilhamento da foto com outros aplicativos

## Observações

Este projeto serve como exemplo prático de uso de câmera em aplicativos móveis com Expo, sendo uma base útil para projetos que envolvam captura de imagens, upload, galeria e compartilhamento de mídias.
