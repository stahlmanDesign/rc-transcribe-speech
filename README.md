# rc-transcribe-speech
Uses the Web Speech API built into most modern browsers to transcribe spoken language.

## Git repository
- https://github.com/stahlmanDesign/rc-transcribe-speech

## Installation
- `npm install --save rc-transcribe-speech`

## Usage
```import TranscribeSpeech from 'rc-transcribe-speech'```
### Basic
```jsx
<TranscribeSpeech
  onResult={ ({ interimTranscript, finalTranscript })=>{ console.log(finalTranscript) }
  continuous={ true }
/>
```
Speak into a microphone and the transcribed dictation will appear in the console.

### Customizing with props	
```jsx
<TranscribeSpeech
  onStart={ ()=>{ console.log('speech started')} }
  onEnd={ ()=>{ console.log('speech ended')} }
  onResult={ ({ interimTranscript, finalTranscript })=>{ this.setState({ transcribedSpeech: finalTranscript })} }
  continuous={ true }
  lang="en-US"
  stop={ false /* NOTE a button could stop this.state.stop */ }
/>
<div>{ this.state.transcribedSpeech }</div>
```
To show text on the screen set state to the finalTranscript result using the onResult event.

## Source

```jsx
TODO

```


## As an NPM module
- Built according to this tutorial to allow publishing the ES6 React JSX code as an NPM module
- https://medium.com/@BrodaNoel/how-to-create-a-react-component-and-publish-it-in-npm-668ad7d363ce
	
