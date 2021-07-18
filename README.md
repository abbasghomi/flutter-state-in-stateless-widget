# State in StateLess widget 

## in Flutter

Handling state in a widget needs it extends StatefulWidget  But if you want to get notified of state changes in a StatelessWidget, you can use ValueNotifier



ValueNotifier definition

```dart
final ValueNotifier<int> _counter = ValueNotifier<int>(0);
```



and using this ValueNotifier in widget tree

```dart
ValueListenableBuilder(
    valueListenable: _counter,
    builder: (context, _, __) {
      return Text(
        '${_counter.value}',
        style: Theme.of(context).textTheme.headline4,
      );
    }),
```

