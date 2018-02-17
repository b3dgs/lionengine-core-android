# LionEngine
[![Build Status](https://travis-ci.org/b3dgs/lionengine.svg?branch=lionengine-android-9.0.0)](https://travis-ci.org/b3dgs/lionengine) ![Coverage](https://img.shields.io/badge/coverage-96%25-brightgreen.svg) ![Lines of code](https://img.shields.io/badge/lines%20of%20code-31k-lightgrey.svg)
[![Maven Central](https://img.shields.io/badge/maven--central-8.4.1-blue.svg)](http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22com.b3dgs.lionengine%22) [![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
<table>
    <tr>
        <td>
            <a href="http://www.b3dgs.com/v7/page.php?lang=en&section=lionengine"><img src="http://www.b3dgs.com/v7/projects/lionengine/lionengine.jpg"/></a>
        </td>
        <td>
            <h4 align="center">Summary</h4>
            <div align="left">
                <ul>
                    <li><a href="#presentation">Presentation</a></li>
                    <li><a href="#download">Download</a></li>
                    <li><a href="#installation">Installation</a></li>
                    <li><a href="#getting-started">Getting Started</a></li>
                    <li><a href="#tutorials">Tutorials</a></li>
                </ul>
            </div>
        </td>
    </tr>
</table>

## Presentation

The __LionEngine__ is a game engine especially developed during the project [Lionheart Remake](http://www.b3dgs.com/v7/page.php?lang=en&section=lionheart_remake) for an easy Java use.
The engine is as a library, in Jar format (_including its javadoc_), which can be included in any project;
for utility class uses, or to directly implement and inherit a game skeleton (_including management of frame rate, extrapolation, input output..._).

Using Java 8 internal libraries, it is specifically designed for 2D games (no support for 3D at the moment), and proposes a set of functions for 2D resources management (_images_, _sprites_, _animations_, _tiles_...).

It supports __Android 7.0__ *(API 24)*.
The only change to perform is the gameplay part, as the '__mouse__' and '__keyboard__' concepts are different on Android.
Everything else is fully compatible and does not require any changes.

<a href="http://lionengine.b3dgs.com/v8-4/page.php?lang=en&section=home"><img src="http://lionengine.b3dgs.com/v8-4/img/home/overview_en.png"/></a>

## Download

* [Go to website](http://www.b3dgs.com/v7/page.php?lang=en&section=lionengine)

## Installation

Steps to include the __LionEngine__ in your project:

1. Download at least [Android Studio 3.0.0](https://developer.android.com/studio/index.html)
2. Include all __LionEngine__ libraries you need for your project, following the tree dependency:
  * __lionengine-core__ _(minimum requirement)_
    * __lionengine-core-android__ _(uses_ __Android 7.0__ _as graphic renderer, target for smartphones)_
3. You are now ready to use the __LionEngine__ in your project

## Getting Started

Once you installed the __LionEngine__ in your project, you may would like to know how to prepare a quick sample as a first try.

#### Main class

* Using __lionengine-core-android__
```java
public class ActivitySample extends ActivityGame
{
    @Override
    protected void start(Bundle bundle)
    {
        EngineAndroid.start("Sample Project", Version.create(0, 1, 0), this);
        Loader.start(Config.fullscreen(Scene.NATIVE), Scene.class);
    }
}
```

#### Minimal sequence
```java
public class Scene extends Sequence
{
    public static final Resolution NATIVE = new Resolution(320, 240, 60);

    public Scene(Context context)
    {
        super(context, NATIVE);
    }

    @Override
    public void load()
    {
        // Load resources
    }

    @Override
    public void update(double extrp)
    {
        // Update game
    }

    @Override
    public void render(Graphic g)
    {
        // Render game
    }
}
```

## Tutorials

* [LionEngine WebSite](http://lionengine.b3dgs.com)
