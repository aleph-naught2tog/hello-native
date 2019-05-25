# hello-native

# react-native notes

## misc notes

* no usable QR data prob means you need the expo client installed

## requirements

* expo client: for running the app on your device
  * [iOs](https://itunes.apple.com/app/apple-store/id982107779)
  * [android](https://play.google.com/store/apps/details?id=host.exp.exponent&referrer=www)

For something similar to `create-react-app`, you need the expo CLI itself to bootstrap. For that you can run: `npm install --global expo-cli` -- otherwise you should be able to just pull this down and run `npm start`.

## working on a project

1. `npm start` starts the server/bundler
2. once it's loaded, you scan the qr code with your phone; on an iPhone, you just need to open your camera and get the QR code in focus. A little dialogue should pop up that says 'Open in EXPO'.

### fyi

The page that opens in your browser from the terminal is basically the console. You can show either the server logs or the server log + the log for the device (which looks so far like it's more akin to the browser console not surprisingly -- eg, React stack traces show up in here.)

It should have a thing about connection type -- set to `LAN` most likely.

### issues
* if you get an error about how the QR code contains no usable data, make sure you have the expo client installed on your phone and try starting/stopping the server.
* make sure you are on the same network on your device as you are on the computer you're using

## notes

* yes there's live reloading apparently
* strings and text must be wrapped in a `Text` component. eg:
  ```jsx
  // this is OK
  const SomeOkaything = (
    <View>
      <Text>hello world</Text>
    </View>
  );

  // Invariant Violation: Text strings must be rendered within a <Text> component.
  const SomeBadThing = (
    <View>
      i'm wrong :(
    </View>
  );
  ```

