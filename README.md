- 👋 Hi, I’m @Buyndelger-222
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Buyndelger-222/Buyndelger-222 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

// Copyright 2018 The Flutter team. All rights reserved.
// Use of this source code is governed by a BSD-style license that can be
// found in the LICENSE file.

import 'package:english_words/english_words.dart';
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

// #docregion MyApp
class MyApp extends StatelessWidget {
  const MyApp({super.key});

  // #docregion build
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'ХАБЭА-н зөвлөмж мэдээлэл',
      home: Scaffold(
        appBar: AppBar(
          title: const Text('ХАБЭА-н зөвлөмж мэдээлэл'),
        ),
        body: const Center(
          child: RandomWords(),
        ),
      ),
    );
  }
  // #enddocregion build
}
// #enddocregion MyApp

// #docregion RandomWordsWidget
// #docregion RandomWords
class RandomWords extends StatefulWidget {
  const RandomWords({super.key});

  @override
  State<RandomWords> createState() => _RandomWordsState();
}
// #enddocregion RandomWords

// #docregion _RandomWordsState, RWS-class-only
class _RandomWordsState extends State<RandomWords> {
  // #enddocregion RWS-class-only
  @override
  Widget build(BuildContext context) {
    final wordPair = WordPair.random();
    return Text(wordPair.asPascalCase);
  }
  // #docregion RWS-class-only
}
// #enddocregion _RandomWordsState, RWS-class-only
// #enddocregion RandomWordsWidget

