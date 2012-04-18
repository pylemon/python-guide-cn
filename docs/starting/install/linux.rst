.. _install-linux:

在 Linux 上安装 Python
======================

最新版本的 Ubuntu, **在系统中已经提供了 Python 2.7**.

你不需要安装或者配置任何东西来使用 Python. 尽管如此, 我会强烈建议你在开始构建您的应用之前, 安装下一节中提到的工具和库. 特别是, 你总是应该安装 Distribute, 这会让你更容易的使用其他的第三方 Python 库.

Distribute & Pip
----------------

在所有第三方 Python 软件中最为重要的是 Distribute, 它扩展了在标准库中的 disttils 所提供的打包和安装的基本功能. 一旦你将 Distribute 加入到你的 Python 系统中, 你就可以仅使用一条命令, 下载和安装任何复杂的 Python 软件产品. 它同时允许你以很小的代价将这种网络安装能力加入到你自己的 Python 软件中去.

在 Linux 上获取最新版本的 Distribute, 请运行下面的 python 脚本:
    http://python-distribute.org/distribute_setup.py

目前使用的 ``easy_install`` 命令已经被许多人认为已经废弃, 因此我们将安装它的替代品: **pip**. 不同于 ``easy_install`` 的是 Pip 允许卸载安装过的包, 而且正被积极的维护.

安装 pip, 只需要打开命令行并运行::

    $ easy_install pip


Virtualenv
----------

在安装好 Distribute & Pip 之后, 下一个你应该安装的开发工具是 `virtualenv <http://pypi.python.org/pypi/virtualenv/>`_. 使用 pip::

    $ pip install virtualenv

virtualenv 工具包提供了创建虚拟 Python 环境的能力, 虚拟环境不会互相影响或是影响到系统中安装的 Python. 如果你在开始开始编码之前安装了 virtualenv 你会习惯去使用它为每一个项目创建一个完全干净的 Python 环境. 这对于在框架和应用有众多依赖的 Web 开发中显得尤为重要.

建立一个新的 Python 环境, 需要切换任何你想要存储这个环境的目录中, 并在你的项目目录中运行 virtualenv::

    $ virtualenv --distribute venv

使用这个环境, 运行 ``source venv/bin/activate``. 在你的命令提示符会显示当前激活的环境. 一旦你完成在当前虚拟环境中的工作, 运行 ``deactivate`` 还原到普通设置.

每一个新的环境会自动包含一个复制的 ``pip``, 因此你能够安装你想在那个环境中使用的第三方库和工具. 你可以将自己的代码放到环境中的一个子目录中去. 当你不再需要一个特定的环境, 只需要复制出你的代码, 删除到环境的主目录既可.

--------------------------------

This page is a remixed version of `another guide <http://www.stuartellis.eu/articles/python-development-windows/>`_, which is available under the same license.

