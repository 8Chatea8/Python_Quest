# Code Peer Review Templete
- 코더 : 차정은
- 리뷰어 : 김재림


# PRT(PeerReviewTemplate)
각 항목을 스스로 확인하고 체크하고 확인하여 작성한 코드에 적용하세요.
- [x] 1.코드가 정상적으로 동작하나요?
- [x] 2.문제를 제대로 이해했나요? 
- [x] 3.함수가 작동하는 방식을 잘 설명했나요?
- [x] 4.발생 가능한 에러를 찾아서 디버깅을 했나요?
- [x] 5.코드를 더 개선시켰나요?

# 예시
1. 코드의 작동 방식을 주석으로 기록합니다.
2. 코드의 작동 방식에 대한 개선 방법을 주석으로 기록합니다.
3. 참고한 링크 및 ChatGPT 프롬프트 명령어가 있다면 주석으로 남겨주세요.
```python
# 사칙 연산 계산기

        "# Fish 클래스\n",
        "\n",
        "class Fish:\n",
        "  def __init__(self, name, speed):\n",
        "    self.name = name\n",
        "    self.speed = speed\n",
        "  \n",
        "  def movement(self):\n",
        "    print(f\"{self.name} is swimming at {self.speed} m/s\")"
      ]
    },
    {
      "cell_type": "markdown",
      "source": [
        "#컨프리헨션 만들기\n",
        "```python\n",
        "[표현식 for 항목 in iterable if 조건식]\n",
        "```\n"
      ],
      "metadata": {
        "id": "BgrtX2ZWncBL"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# 컴프리헨션 사용해서 출력하는 함수\n",
        "\n",
        "def show_fish_movement_comprehension(fish_list):\n",
        "  [i.movement() for i in fish_list]"
      ],
      "metadata": {
        "id": "x5lXq--vl12w"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "markdown",
      "source": [
        "#이터레이터 만들기\n",
        "```python\n",
        "my_list = [1, 2, 3, 4, 5]\n",
        "\n",
        "# 리스트를 이터레이터로 변환\n",
        "my_iterator = iter(my_list)\n",
        "\n",
        "# 이터레이터 사용\n",
        "print(next(my_iterator))  # 1\n",
        "print(next(my_iterator))  # 2\n",
        "print(next(my_iterator))  # 3\n",
        "```"
      ],
      "metadata": {
        "id": "sttT7Pvlrgeo"
      }
    },
    {
      "cell_type": "code",
      "source": [
        "# 이터레이터 사용해서 출력하는 함수\n",
        "\n",
        "def show_fish_movement_iterator(fish_list):\n",
        "  fish_iter = iter(fish_list)\n",
        "  for i in range(len(fish_list)):\n",
        "    fish_iter.__next__().movement()"
      ],
      "metadata": {
        "id": "pe5yhf2sqbwY"
      },
      "execution_count": null,
      "outputs": []
    },
    {
      "cell_type": "code",
      "source": [
        "# 제너레이터 사용해서 출력하는 함수\n",
        "\n",
        "# def show_fish_movement_generator(fish_list):\n",
        "#   (i.movement() for i in fish_list)\n",
        "#   def fish_generator(obj):\n",
        "#     yield obj.movement()\n",
        "#   for i in fish_list:\n",
        "#     fish_generator(i)\n",
        "#     print(fish_generator(i))\n",
        "\n",
        "# def show_fish_movement_generator(fish_list):\n",
        "#     def fish_movement_generator():\n",
        "#         for fish in fish_list:\n",
        "#             yield fish\n",
        "#     fish_movement_generator(fish_list).movement()\n",
        "\n",
        "\n",
        "# show_fish_movement_generator(fish_list)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/",
          "height": 358
        },
        "id": "xBCPHoOPx43O",
        "outputId": "708b9c18-fb9d-43a0-d396-c398ff783f76"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "error",
          "ename": "TypeError",
          "evalue": "ignored",
          "traceback": [
            "\u001b[0;31m---------------------------------------------------------------------------\u001b[0m",
            "\u001b[0;31mTypeError\u001b[0m                                 Traceback (most recent call last)",
            "\u001b[0;32m<ipython-input-45-0ac6bec21e60>\u001b[0m in \u001b[0;36m<cell line: 18>\u001b[0;34m()\u001b[0m\n\u001b[1;32m     16\u001b[0m \u001b[0;34m\u001b[0m\u001b[0m\n\u001b[1;32m     17\u001b[0m \u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0;32m---> 18\u001b[0;31m \u001b[0mshow_fish_movement_generator\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0mfish_list\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0m",
            "\u001b[0;32m<ipython-input-45-0ac6bec21e60>\u001b[0m in \u001b[0;36mshow_fish_movement_generator\u001b[0;34m(fish_list)\u001b[0m\n\u001b[1;32m     13\u001b[0m         \u001b[0;32mfor\u001b[0m \u001b[0mfish\u001b[0m \u001b[0;32min\u001b[0m \u001b[0mfish_list\u001b[0m\u001b[0;34m:\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[1;32m     14\u001b[0m             \u001b[0;32myield\u001b[0m \u001b[0mfish\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0;32m---> 15\u001b[0;31m     \u001b[0mfish_movement_generator\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0mfish_list\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m.\u001b[0m\u001b[0mmovement\u001b[0m\u001b[0;34m(\u001b[0m\u001b[0;34m)\u001b[0m\u001b[0;34m\u001b[0m\u001b[0;34m\u001b[0m\u001b[0m\n\u001b[0m\u001b[1;32m     16\u001b[0m \u001b[0;34m\u001b[0m\u001b[0m\n\u001b[1;32m     17\u001b[0m \u001b[0;34m\u001b[0m\u001b[0m\n",
            "\u001b[0;31mTypeError\u001b[0m: show_fish_movement_generator.<locals>.fish_movement_generator() takes 0 positional arguments but 1 was given"
          ]
        }
      ]
    },
    {
      "cell_type": "code",
      "source": [
        "# 물고기 리스트\n",
        "fish_list = [\n",
        "    Fish(\"Nemo\", 3),\n",
        "    Fish(\"Dory\", 5),\n",
        "    Fish(\"Marlin\", 7),\n",
        "    Fish(\"Bubbles\", 2),\n",
        "    Fish(\"Gill\", 4)\n",
        "]\n",
        "\n",
        "\n",
        "# 물고기들의 움직임 출력\n",
        "print(\"Using Comprehension:\")\n",
        "show_fish_movement_comprehension(fish_list)\n",
        "\n",
        "print(\"\\nUsing Iterator:\")\n",
        "show_fish_movement_iterator(fish_list)"
      ],
      "metadata": {
        "colab": {
          "base_uri": "https://localhost:8080/"
        },
        "id": "Bv74cNkckBzW",
        "outputId": "c3462f3e-25b3-48ab-b27d-923225443ec6"
      },
      "execution_count": null,
      "outputs": [
        {
          "output_type": "stream",
          "name": "stdout",
          "text": [
            "Using Comprehension:\n",
            "Nemo is swimming at 3 m/s\n",
            "Dory is swimming at 5 m/s\n",
            "Marlin is swimming at 7 m/s\n",
            "Bubbles is swimming at 2 m/s\n",
            "Gill is swimming at 4 m/s\n",
            "\n",
            "Using Iterator:\n",
            "Nemo is swimming at 3 m/s\n",
            "Dory is swimming at 5 m/s\n",
            "Marlin is swimming at 7 m/s\n",
            "Bubbles is swimming at 2 m/s\n",
            "Gill is swimming at 4 m/s\n"
          ]
        }
      ]
    }
  ]
}
```

# 참고 링크 및 코드 개선 여부
```python
# 제너레이터 구현하는 것에서 더 조사해서 성공했으면 좋겠습니다!
# 다양한 코드를 쓰셔서 새롭게 알게되었습니다.
#
#
```
