# Backend Flask API

@app.route('/devices/<int:id>', methods=['POST'])

def update_device(id):

 status = request.json['status']

 c.execute('UPDATE devices SET status = ? WHERE id = ?', (status, id))

 conn.commit()
 return jsonify({'message': 'Device updated'})

# ESP32 script example

import urequests

sensor.measure()

temp = sensor.temperature()

urequests.post('http://<server-ip>:5000/sensors/1', json={'value': str(temp)})# Smart-building-management.
