# codeclause
import numpy as np
hsv = cv2.cvtColor(img, cv2.COLOR_BGR2HSV)
color = np.uint8([[[b,g,r]]])
hsv_color = cv2.cvtColor(color,cv2.COLOR_BGR2HSV)
lower_range = np.array([hsv_color[0][0][0] - 10,100,100])
upper_range = np.array([hsv_color[0][0][0] + 10,255,255])

mask = cv2.inRange(hsv, lower_range, upper_range)

cv2.imshow('mask', mask)
cv2.waitKey(0)
cv2.destroyAllWindows()
