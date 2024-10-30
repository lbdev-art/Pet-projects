from google.colab import drive
drive.mount('/content/drive')


from matplotlib import font_manager
print("List of all fonts currently available in the matplotlib:")
print(*font_manager.findSystemFonts(fontpaths=None, fontext='ttf'), sep="")


import matplotlib.pyplot as plt
from matplotlib import font_manager as fm
# funnel chart
y = [5,4,3,2,1]
x = [97,77,54,29,15]
labels = ['Hot Leads', 'Samples Sent', 'Quotes', 'Negotiations', 'Sales']
x_max = 100
x_min = 0
x_range = x_max - x_min
fpath = "/content/drive/MyDrive/content/fonts/Humor-Sans.ttf"
font = fm.FontProperties(fname=fpath)

fig, ax = plt.subplots(1, figsize=(12,6))
for idx, val in enumerate(x):
    left = (x_range - val)/2
    plt.barh(y[idx], x[idx], left = left,
             color='#808B96', height=.8)
    # label
    plt.text(50, y[idx]+0.1, labels[idx], ha='center',
             fontproperties=font, fontsize=16, color='#2A2A2A')
    # value
    plt.text(50, y[idx]-0.3, x[idx], ha='center',
             fontproperties=font, fontsize=16, color='#2A2A2A')

    if idx != len(x)-1:
        next_left = (x_range - x[idx+1])/2
        shadow_x = [left, next_left,
                    100-next_left, 100-left, left]

        shadow_y = [y[idx]-0.4, y[idx+1]+0.4,
                    y[idx+1]+0.4, y[idx]-0.4, y[idx]-0.4]
        plt.fill(shadow_x, shadow_y, color='grey', alpha=0.6)
plt.xlim(x_min, x_max)
plt.axis('off')
plt.title('Seloff Inc.', fontproperties=font, loc='center', fontsize=24, color='#2A2A2A')
plt.show()
